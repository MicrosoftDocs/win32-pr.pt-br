---
description: Uma instalação administrativa cria uma imagem de origem de um aplicativo ou produto em uma rede.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02c8e3eb606dc92c60a86dd8e3216cbc99603200a87e5ee5dda0983fb7ad34d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559156"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a>Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa

Uma [instalação administrativa](administrative-installation.md) cria uma imagem de origem de um aplicativo ou produto em uma rede. Os usuários em um grupo de trabalho que têm acesso a essa imagem administrativa podem instalar o produto dessa fonte. A atualização do aplicativo para esse grupo de trabalho é feita em duas etapas:

-   Primeiro, o patch de atualização pequena pode ser aplicado à imagem administrativa.
-   Em segundo lugar, as alterações na atualização pequena precisam ser propagadas para os usuários.

**Para aplicar um patch de atualização pequeno a uma imagem administrativa**

1.  Obtenha a pequena atualização na forma de um [pacote de patch](patch-packages.md). Por exemplo, a pequena atualização chamada patch. msp.
2.  Obtenha o caminho para a imagem administrativa.
3.  A partir da linha de comando, use:

    **msiexec/a** *\[ caminho para a imagem administrativa .msi \] arquivo* **/p** *patch. msp*

4.  Isso atualiza os arquivos de aplicativo e o arquivo de .msi da imagem administrativa. Para obter uma lista das opções que podem ser usadas com Msiexec.exe, consulte [Opções de linha de comando](command-line-options.md). Windows O instalador determina automaticamente se a imagem administrativa está usando nomes de arquivo curtos e define a propriedade [**SHORTFILENAMES**](shortfilenames.md) .
5.  A imagem administrativa resultante é a mesma que a produzida por uma instalação administrativa usando um CD-ROM completo do produto que inclui a atualização. Quando novos usuários instalam o aplicativo dessa fonte, eles recebem o aplicativo atualizado.

**Para propagar a pequena atualização para o grupo de trabalho**

-   Os membros do grupo de trabalho obtêm as alterações reinstalando o aplicativo da imagem administrativa usando o procedimento descrito em [aplicando pequenas atualizações reinstalando o produto](applying-small-updates-by-reinstalling-the-product.md).

 

 



