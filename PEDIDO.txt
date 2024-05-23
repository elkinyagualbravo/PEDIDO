package org.example;

import java.util.Date;

public class Pedido {
    private int idPedido;
    private Date fecha;
    private double total;
    private String estado;

    public Pedido(int idPedidoC, Date fechaC, double totalC, String estadoC) {
        this.idPedido = idPedidoC;
        this.fecha = fechaC;
        this.total = totalC;
        this.estado = estadoC;
    }

    public void solicitar() {
        this.estado = "Solicitado";
        System.out.println("El pedido ha sido solicitado");
    }

    public void cancelarPedido() {
        if (!this.estado.equals("Cancelado")) {
            this.estado = "Cancelado";
            System.out.println("Cancelado con éxito");
        } else {
            System.out.println("El pedido ya fue cancelado");
        }

    }

    public double calcularTotal() {
        System.out.println("Calculando pedido");
        return this.total;
    }

    public void reiniciarEstado() {
        this.estado = "Sin estado...";
        System.out.println("El pedido no tiene estado");
    }

    public int getIdPedido() {
        return this.idPedido;
    }

    public String toString() {
        return "Pedido{idPedido=" + this.idPedido + ", fecha=" + this.fecha + ", total=" + this.total + ", estado='" + this.estado + "'}";
    }

    public void setIdPedido(int idPedido) {
        this.idPedido = idPedido;
    }

    public Date getFecha() {
        return this.fecha;
    }

    public void setFecha(Date fecha) {
        this.fecha = fecha;
    }

    public double getTotal() {
        return this.total;
    }

    public void setTotal(double total) {
        this.total = total;
    }

    public String getEstado() {
        return this.estado;
    }

    public void setEstado(String estado) {
        this.estado = estado;
    }
}
