---
description: Encapsular o disco rígido em um único arquivo para uso pelo sistema operacional como um disco virtual. Os discos virtuais podem funcionar como discos de inicialização e podem hospedar sistemas de arquivos nativos (NTFS, FAT, exFAT e UDFS) ao mesmo tempo que suportam operações padrão de disco e arquivo.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Disco Virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfa2d39ea786029e8be319d7affaa2214682ce05
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480982"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Disco Virtual

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Finalidade

O formato VHD (Disco Rígido Virtual) é uma especificação de formato de imagem disponível publicamente que especifica um disco rígido virtual encapsulado em um único arquivo, capaz de hospedar sistemas de arquivos nativos ao mesmo tempo que suporta operações padrão de disco e arquivo. Um exemplo de como os arquivos VHD são usados é o recurso [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) no Windows Server 2008, Servidor Virtual e Windows Virtual PC. Esses produtos usam VHDs para conter a Windows do sistema operacional utilizada por uma máquina virtual como seu disco de inicialização do sistema.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Público de desenvolvedores

O SDK (Software Development Kit) do Microsoft Windows integra o suporte ao VHD nativo para trabalhar com VHDs, facilitando para desenvolvedores e administradores criar, gerenciar e implantar imagens Windows em VHDs usando o suporte à API de plataforma ou ferramentas de gerenciamento. Não é necessário instalar aplicativos separados ou implementar um analisador de formato VHD para habilitar essas operações. Essas APIs permitem o uso genérico de VHDs independentes de qualquer outra tecnologia de virtualização.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Requisitos de tempo de execução

O VHD tem suporte no Windows 7 e Windows Server 2008 R2.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>Nesta seção


| Tópico | Descrição | 
|-------|-------------|
| <p><a href="about-vhd.md">Sobre o VHD</a></p> | <p>Descreve o formato VHD com dicas e sugestões de uso de API.</p> | 
| <p><a href="vhd-reference.md">Referência de VHD</a></p> | <p>Descreve as funções, estruturas e enumerações da API vhD.</p> | 


 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Tópicos relacionados

[Serviço de Disco Virtual](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
