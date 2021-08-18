---
description: 'Windows O instalador permite que uma instância de um código de produto seja instalada por contexto e os dois tipos possíveis de contexto são o seguinte: MachineUser Se um código do produto permanecer inalterado, apenas uma instância poderá ser instalada no contexto do computador e apenas uma instância poderá ser instalada em cada contexto do usuário. Para que várias instâncias permaneçam isoladas, elas devem ter códigos de produto diferentes e não podem compartilhar dados de arquivo ou dados não arquivos. O Windows instalador não pode instalar várias instâncias de produtos usando instalações simultâneas. No entanto, você pode instalar várias instâncias de um produto se tiver um pacote de instalação separado para cada instância de um produto ou patch. Em seguida, cada pacote pode manter seu próprio conjunto de dados e ter seu próprio código de produto exclusivo. Começando com o instalador executando o Windows Server 2003 e o Windows XP com Service Pack 1 (SP1), você pode instalar várias instâncias de um produto usando as transformaçãos de código do produto e um pacote .msi ou um patch. Você também pode usar as transformação de código do produto para instalar várias instâncias de um produto com o Windows 2000 com o Service Pack 4 (SP4) e o Windows Installer&\# 160; 3.0. A única maneira de instalar mais de uma instância de um produto com versões anteriores do instalador é ter um pacote de instalação separado para cada instância. O uso de transformaçãos de instância reduz significativamente o esforço necessário para dar suporte a várias instâncias de um produto. Você pode autor de um pacote base Windows Instalador para um produto e, em seguida, várias transformações de instância que alteram o código do produto e gerenciam dados para cada instância. Para obter mais informações, consulte Authoring Multiple Instances with Instance Transforms and Installing Multiple Instances with Instance Transforms.'
ms.assetid: 5147ecbd-c395-4a8f-972d-f5c5b2173eff
title: Instalando várias instâncias de produtos e patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c9f061ef203effc4ec71c386f17a4c92bae957610fdc3a15b0c64a92e1e024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946144"
---
# <a name="installing-multiple-instances-of-products-and-patches"></a>Instalando várias instâncias de produtos e patches

Windows O instalador permite que uma instância de um código de produto seja instalada por contexto e os dois tipos possíveis de contexto são os seguintes:

-   Computador
-   Usuário

Se um código do produto permanecer inalterado, apenas uma instância poderá ser instalada no contexto do computador e apenas uma instância poderá ser instalada em cada contexto de usuário.

Para que várias instâncias permaneçam isoladas, elas devem ter códigos de produto diferentes e não podem compartilhar dados de arquivo ou dados não arquivos. O Windows instalador não pode instalar várias instâncias de produtos usando [instalações simultâneas](concurrent-installations.md). No entanto, você pode instalar várias instâncias de um produto se tiver um pacote de instalação separado para cada instância de um produto ou patch. Em seguida, cada pacote pode manter seu próprio conjunto de dados e ter seu próprio código de produto exclusivo.

Começando com o instalador executando o Windows Server 2003 e o Windows XP com Service Pack 1 (SP1), você pode instalar várias instâncias de um produto usando as transformaçãos de código do produto e um pacote .msi ou um patch. Você também pode usar as transformação de código do produto para instalar várias instâncias de um produto com o Windows 2000 com Service Pack 4 (SP4) e Windows Installer 3.0. A única maneira de instalar mais de uma instância de um produto com versões anteriores do instalador é ter um pacote de instalação separado para cada instância.

O uso de transformaçãos de instância reduz significativamente o esforço necessário para dar suporte a várias instâncias de um produto. Você pode autor de um pacote Windows instalador base para um produto e, em seguida, várias transformares de instância que alteram o código do produto e gerenciam dados para cada instância.

Para obter mais informações, [consulte Authoring Multiple Instances with Instance Transforms](authoring-multiple-instances-with-instance-transforms.md) [and Installing Multiple Instances with Instance Transforms](installing-multiple-instances-with-instance-transforms.md).

 

 



