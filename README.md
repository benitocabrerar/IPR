# Análisis de Desempeño de Pozos Petroleros
## Simulador de Curvas IPR y VFP

## Descripción

Esta aplicación web permite realizar análisis avanzados del desempeño de pozos petroleros mediante la generación, visualización e interpretación de curvas IPR (Inflow Performance Relationship) y VFP (Vertical Flow Performance). La herramienta implementa metodologías estándar de la industria para determinar si un pozo puede fluir naturalmente o requiere sistemas de levantamiento artificial.

## Características Principales

- **Modelado de IPR**: Implementación del método de Vogel para modelar el comportamiento de flujo de entrada al pozo.
- **Análisis VFP**: Generación de curvas de comportamiento de flujo vertical para diferentes diámetros de tubería.
- **Punto de Operación**: Cálculo automatizado de la intersección entre curvas IPR y VFP para determinar el punto operativo del pozo.
- **Correlaciones PVT**: Implementación de correlaciones estándar de la industria (Standing, Glaso, Vasquez-Beggs, Petrosky-Farshad) para el cálculo de propiedades de fluidos.
- **Exportación de Resultados**: Generación de reportes en formato PDF y Excel para documentación y análisis posterior.
- **Análisis de Datos de Prueba**: Incorporación de datos reales de pruebas de pozo para validación del modelo.

## Conformidad con Estándares de la Industria

Esta aplicación ha sido desarrollada siguiendo los estándares y prácticas recomendadas internacionales para la industria petrolera:

- **API RP 11V6**: Diseño de Sistemas de Levantamiento Artificial por Gas.
- **API RP 19G1-19G2**: Evaluación de Comportamiento de Pozos y Reservorios.
- **SPE Monograph 1**: Optimización del Análisis de Sistemas de Producción.
- **ISO 13500/13503/13628**: Estándares para Equipos de Producción Petrolera.
- **NORSOK D-010**: Estándares para Integridad de Pozos.

## Fundamentos Técnicos

### Modelo IPR de Vogel

El modelo implementa la ecuación de Vogel para yacimientos subsaturados:

```
q/qmax = 1 - 0.2(Pwf/Pr) - 0.8(Pwf/Pr)²
```

Donde:
- `q` = Caudal de producción a una presión de fondo específica
- `qmax` = Caudal máximo teórico (a Pwf = 0)
- `Pwf` = Presión de fondo fluyente
- `Pr` = Presión promedio del reservorio

### Análisis VFP

Las curvas VFP se generan considerando:
- Pérdidas por fricción (ecuación de Fanning)
- Pérdidas por elevación (gradiente hidrostático)
- Efectos de transferencia de energía cinética

### Índice de Productividad (PI)

Se calculan tanto el PI simplificado como el complejo:

```
PI = 7.08×10⁻³ × k × h / (μ × ln(re/rw))
```

Donde:
- `k` = Permeabilidad (md)
- `h` = Espesor neto de formación (ft)
- `μ` = Viscosidad del fluido (cp)
- `re` = Radio de drenaje (ft)
- `rw` = Radio del pozo (ft)

## Requisitos del Sistema

- Navegador web moderno compatible con HTML5
- Conexión a Internet para cargar las bibliotecas necesarias
- Se recomienda una pantalla con resolución mínima de 1280x768

## Instalación y Uso

1. Clone este repositorio:
   ```bash
   git clone https://github.com/usuario/analisis-pozos-petroleros.git
   ```

2. Abra el archivo `index.html` en su navegador, o implemente en un servidor web.

3. Complete los parámetros del pozo y yacimiento en el formulario.

4. Visualice y analice los resultados en tiempo real.

## Validación y Verificación

La aplicación ha sido validada contra casos de estudio publicados por la Society of Petroleum Engineers (SPE) y el American Petroleum Institute (API), garantizando resultados consistentes con los estándares de la industria. Los cálculos han sido contrastados con software comercial como PIPESIM™, PROSPER™ y NODAL™.

## Referencias Técnicas

1. Vogel, J.V.: "Inflow Performance Relationships for Solution-Gas Drive Wells," JPT (Jan. 1968) 83-92.
2. Standing, M.B.: "Volumetric and Phase Behavior of Oil Field Hydrocarbon Systems," Society of Petroleum Engineers (1977).
3. Brown, K.E.: "The Technology of Artificial Lift Methods," PennWell Publishing Co., Tulsa (1984).
4. Beggs, H.D. and Brill, J.P.: "A Study of Two-Phase Flow in Inclined Pipes," JPT (May 1973) 607-617.
5. Golan, M. and Whitson, C.H.: "Well Performance," Prentice Hall, Englewood Cliffs, N.J. (1991).

## Limitaciones y Consideraciones

- La aplicación utiliza correlaciones empíricas que pueden tener rangos de validez específicos.
- Se recomienda validar los resultados con datos de campo para aplicaciones críticas.
- Los efectos no-Darcy y de daño de formación (skin) están incluidos de forma simplificada.

## Contribuciones

Las contribuciones son bienvenidas. Para cambios importantes:

1. Abra un issue para discutir el cambio propuesto.
2. Envíe un pull request con sus modificaciones.
3. Asegúrese de actualizar las pruebas según corresponda.
4. Documente adecuadamente los cambios realizados.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT - vea el archivo LICENSE para más detalles.

## Contacto

Para consultas técnicas o comerciales, contacte a:

Ing. Benito Cabrera R.  MBA
Master en Petróleos Mención en Procesos de Producción e Industrialización de Hidrocarburos
Master en Administración de Empresas con especialización en Finanzas y Planificación Estratégica
Master MBA Global en Políticas Públicas 
Ingeniero en Petróleos
Email: benito.cabrera@petrolatina.com  
PetroLatina S.A.

---

© 2024 PetroLatina S.A. Todos los derechos reservados.
