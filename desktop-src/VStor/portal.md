---
description: Encapsular o disco rígido em um único arquivo para uso pelo sistema operacional como um disco virtual. Os discos virtuais podem funcionar como discos de inicialização e podem hospedar sistemas de arquivos nativos (NTFS, FAT, exFAT e UDFS) enquanto dão suporte a operações de arquivo e disco padrão.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Disco Virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044145f5d631b878b533bbd409fad5eda5b4863f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164489"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Disco Virtual

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Objetivo

O formato VHD (disco rígido virtual) é uma especificação de formato de imagem disponível publicamente que especifica um disco rígido virtual encapsulado em um único arquivo, capaz de hospedar sistemas de arquivos nativos enquanto dá suporte a operações de disco e arquivo padrão. Um exemplo de como os arquivos VHD são usados é o recurso do [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) no windows Server 2008, no Virtual Server e no Windows Virtual PC. Esses produtos usam VHDs para conter a imagem do sistema operacional Windows utilizada por uma máquina virtual como seu disco de inicialização do sistema.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Público de desenvolvedores

O SDK (Software Development Kit) do Microsoft Windows integra o suporte nativo do VHD para trabalhar com VHDs, facilitando para os desenvolvedores e administradores a criação, o gerenciamento e a implantação de imagens do Windows em VHDs usando o suporte à API de plataforma ou as ferramentas de gerenciamento. Não é necessário instalar aplicativos separados ou implementar um analisador de formato VHD para habilitar essas operações. Essas APIs permitem o uso genérico de VHDs independentemente de qualquer outra tecnologia de virtualização.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Requisitos de tempo de execução

O VHD tem suporte no Windows 7 e no Windows Server 2008 R2.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>Nesta seção

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="about-vhd.md">Sobre o VHD</a></p></td>
<td><p>Descreve o formato VHD com dicas e sugestões de uso de API.</p></td>
</tr>
<tr class="even">
<td><p><a href="vhd-reference.md">Referência do VHD</a></p></td>
<td><p>Descreve as funções, estruturas e enumerações da API do VHD.</p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Tópicos relacionados

[Serviço de Disco Virtual](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
