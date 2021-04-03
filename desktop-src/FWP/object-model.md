---
title: Modelo de Objeto
description: A tabela a seguir lista os tipos de objeto que podem ser manipulados por meio de vários conjuntos de API fornecidos pela WFP (Windows Filtering Platform).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007156"
---
# <a name="object-model"></a>Modelo de Objeto

A tabela a seguir lista os tipos de objeto que podem ser manipulados por meio de vários conjuntos de API fornecidos pela WFP (Windows Filtering Platform).



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de objeto</th>
<th>Descrição</th>
<th>Propriedades de exemplo</th>
<th>Exemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Filtrar</td>
<td>Uma regra que governa a classificação. Se as condições forem atendidas, a ação será invocada. <br/> Esse é o objeto mais complexo exposto pela WFP, já que ele une todos os outros tipos de objeto. <br/></td>
<td><ul>
<li>Matriz de condições</li>
<li>Ação (permitir, bloquear, texto explicativo)</li>
<li><a href="filter-weight-assignment.md">Weight</a></li>
<li>Contexto</li>
</ul></td>
<td>&quot;Bloquear o tráfego com uma porta TCP maior que 1024.&quot; <br/> &quot;Texto explicativo para IDS de todo o tráfego não protegido.&quot;<br/></td>
</tr>
<tr class="even">
<td>Balão</td>
<td>Um conjunto de funções que participam do processo de classificação.<br/> Ele permite que o processamento de pacotes personalizado seja feito quando determinadas condições forem atendidas.<br/></td>
<td><ul>
<li>ID</li>
<li>Camada aplicável</li>
</ul></td>
<td>O driver NAT<br/></td>
</tr>
<tr class="odd">
<td>Camada</td>
<td>Um contêiner de filtro no mecanismo de filtro. <br/> Representa um ponto específico no processamento de tráfego de rede em que o mecanismo de filtro é invocado.<br/></td>
<td><ul>
<li>Esquema para filtros que podem ser adicionados à camada</li>
</ul></td>
<td>A camada de transporte de entrada<br/></td>
</tr>
<tr class="even">
<td>Subcamada</td>
<td>Um subcomponente de uma camada, usado na <a href="filter-arbitration.md">arbitragem de filtro</a>.<br/></td>
<td><ul>
<li>Peso</li>
</ul></td>
<td>A subcamada de túnel IPsec<br/></td>
</tr>
<tr class="odd">
<td>Provedor</td>
<td>Um provedor de política que criou uma solução em WFP.<br/> Ele é usado unicamente para gerenciamento; Ele não afeta o processamento de pacotes em tempo de execução.<br/></td>
<td><ul>
<li>ID</li>
<li>Nome do serviço</li>
</ul></td>
<td>Firewall do Windows com Advanced Security<br/> Um aplicativo de filtragem de URL de terceiros<br/></td>
</tr>
<tr class="even">
<td>Contexto do provedor</td>
<td>Um blob de dados usado por um provedor de política para armazenar informações de contexto arbitrários. <br/> Ele é usado para passar informações de configuração personalizadas para um texto explicativo.<br/> A maneira mais comum de usar as informações de contexto é fazer com que os filtros façam referência a um contexto de provedor. <br/></td>
<td><ul>
<li>ID</li>
<li>Blob de dados</li>
</ul></td>
<td>O IPsec armazena as configurações de autenticação no mecanismo de filtragem base (BFE). A &quot; &quot; Propriedade Context de um filtro indica as configurações de autenticação a serem usadas para o tráfego que o filtro descreve.<br/> O Shim de seleção de certificação SSL armazenará informações de certificação em um contexto de provedor. <br/></td>
</tr>
</tbody>
</table>



 

Os tipos de objeto expostos pela API WFP têm semânticas consistentes. As ações de adicionar, enumerar, assinar e assim por diante são semelhantes para todos os tipos de objeto.

Cada tipo de objeto é representado por uma estrutura de dados (por exemplo, [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)). Para minimizar o número de diferentes estruturas de dados expostas pela API WFP, a mesma estrutura de dados é usada para adicionar novos objetos e recuperar os existentes. Portanto, pode haver campos em cada estrutura de dados que são ignorados ao adicionar um novo objeto, já que esses campos são preenchidos pelo BFE (mecanismo de filtragem base) e não pelo chamador. Por exemplo, uma estrutura de dados **FWPM \_ FILTER0** tem um campo **filterid** que contém o **LUID** do **\_ FILTER0 FWPS** correspondente. Esse **LUID** é atribuído por BFE e, portanto, esse campo é ignorado na chamada para [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de objetos](object-management.md)
</dt> </dl>

 

 





