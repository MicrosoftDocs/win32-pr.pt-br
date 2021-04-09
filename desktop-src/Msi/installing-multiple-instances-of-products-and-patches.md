---
description: 'Windows Installer permite que uma instância de um código de produto seja instalada por contexto, e os dois tipos de contexto possíveis são os seguintes: MachineUser se um código de produto permanece inalterado, apenas uma instância pode ser instalada no contexto da máquina e apenas uma instância pode ser instalada em cada contexto de usuário. Para que várias instâncias permaneçam isoladas, elas devem ter códigos de produto diferentes e não podem compartilhar dados de arquivo ou dados não de arquivo. O Windows Installer não pode instalar várias instâncias de produtos usando instalações simultâneas. No entanto, você pode instalar várias instâncias de um produto se tiver um pacote de instalação separado para cada instância de um produto ou patch. Em seguida, cada pacote pode manter seu próprio conjunto de dados e ter seu próprio código de produto exclusivo. Começando com o instalador que executa o Windows Server 2003 e o Windows XP com Service Pack 1 (SP1), você pode instalar várias instâncias de um produto usando transformações de código do produto e um pacote. msi ou um patch. Você também pode usar as transformações de código do produto para instalar várias instâncias de um produto com o Windows 2000 com Service Pack 4 (SP4) e Windows Installer&\# 160; 3,0. A única maneira de instalar mais de uma instância de um produto com versões anteriores do instalador é ter um pacote de instalação separado para cada instância. O uso de transformações de instância reduz significativamente o esforço necessário para dar suporte a várias instâncias de um produto. Você pode criar um pacote de Windows Installer de base para um produto e, em seguida, várias transformações de instância que alteram o código do produto e gerenciam dados para cada instância. Para obter mais informações, consulte criando várias instâncias com transformações de instância e Instalando várias instâncias com transformações de instância.'
ms.assetid: 5147ecbd-c395-4a8f-972d-f5c5b2173eff
title: Instalando várias instâncias de produtos e patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3a1de5de7cc63d5eed2e191d77915630761561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171493"
---
# <a name="installing-multiple-instances-of-products-and-patches"></a>Instalando várias instâncias de produtos e patches

Windows Installer permite que uma instância de um código de produto seja instalada por contexto, e os dois tipos de contexto possíveis são os seguintes:

-   Computador
-   Usuário

Se um código de produto permanecer inalterado, apenas uma instância poderá ser instalada no contexto da máquina e apenas uma instância poderá ser instalada em cada contexto de usuário.

Para que várias instâncias permaneçam isoladas, elas devem ter códigos de produto diferentes e não podem compartilhar dados de arquivo ou dados não de arquivo. O Windows Installer não pode instalar várias instâncias de produtos usando [instalações simultâneas](concurrent-installations.md). No entanto, você pode instalar várias instâncias de um produto se tiver um pacote de instalação separado para cada instância de um produto ou patch. Em seguida, cada pacote pode manter seu próprio conjunto de dados e ter seu próprio código de produto exclusivo.

Começando com o instalador que executa o Windows Server 2003 e o Windows XP com Service Pack 1 (SP1), você pode instalar várias instâncias de um produto usando transformações de código do produto e um pacote. msi ou um patch. Você também pode usar as transformações de código do produto para instalar várias instâncias de um produto com o Windows 2000 com Service Pack 4 (SP4) e Windows Installer 3,0. A única maneira de instalar mais de uma instância de um produto com versões anteriores do instalador é ter um pacote de instalação separado para cada instância.

O uso de transformações de instância reduz significativamente o esforço necessário para dar suporte a várias instâncias de um produto. Você pode criar um pacote de Windows Installer de base para um produto e, em seguida, várias transformações de instância que alteram o código do produto e gerenciam dados para cada instância.

Para obter mais informações, consulte [criando várias instâncias com transformações de instância](authoring-multiple-instances-with-instance-transforms.md) e [Instalando várias instâncias com transformações de instância](installing-multiple-instances-with-instance-transforms.md).

 

 



