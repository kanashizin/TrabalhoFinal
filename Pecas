/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package com.sgsstudios.Main;

import java.io.Serializable;

/**
 *
 * @author SadBo
 */
public class Pecas implements Serializable{
    
    private static int registrados;
    private int id, categoria;
    private double preco;
    private String nome;
    private Clientes comprador = Clientes.nenhum;
    
    public Pecas(String nome, int categoria, double preco){
        //Declaracoes iniciais
        this.id = registrados;
        registrados++;
        this.nome = nome;
        this.categoria = categoria;
        this.preco = preco;
        
    }
    
    public static void venderPeca(String nomeCliente, String cpf, int idPeca){
        //Verificando se o id existe
        if(idPeca >= 0 && idPeca < registrados){
            //Procurando Cliente Igual
            for (int i = 0; i < Main.clientes.size(); i++) {
                //Verificando se estamos falando do mesmo cliente
                if(cpf.equalsIgnoreCase(Main.clientes.get(i).getCpf())){
                    //Adicioando na lista de compras do cliente
                    Main.clientes.get(i).getCompras().add(Main.estoque.get(idPeca));
                    
                }
                
            }
            //Nao achou nenhum cliente com o mesmo CPF
            if(cpf.length() == 11){
                //Adicionando novo cliente
                Main.clientes.add(new Clientes(nomeCliente,cpf,Main.estoque.get(idPeca)));
            }
        }
        
    }
    
    public static String getCategoriaString(int num){
        //Selecionar Categorias
        switch(num){
            
            case 1:
                return "Processador";
            case 2:
                return "Placa Mae";
            case 3:
                return "Placa de Video";
            case 4:
                return "Fonte";
            case 5:
                return "RAM";
            case 6:
                return "Gabinete";
            case 7:
                return "Acessorio PC";
            case 8:
                return "Monitor";
            case 9:
                return "Periferico";
            default:
                return "Sem categoria";
                
        }
        
        
        
    }

    public static int getRegistrados() {
        return registrados;
    }

    public static void setRegistrados(int registrados) {
        Pecas.registrados = registrados;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public int getCategoria() {
        return categoria;
    }

    public void setCategoria(int categoria) {
        this.categoria = categoria;
    }

    public double getPreco() {
        return preco;
    }

    public void setPreco(double preco) {
        this.preco = preco;
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public Clientes getComprador() {
        return comprador;
    }

    public void setComprador(Clientes comprador) {
        this.comprador = comprador;
    }
    
    
    @Override
    public String toString(){
        //Pegando informacoes da peca
        String str = id+" | "+nome+" | R$"+preco+" | " + this.getCategoriaString(categoria) + " | Comprador: " + comprador.getNome();
        return str;
        
    }
    
}
