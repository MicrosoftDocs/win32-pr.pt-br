---
description: Uma pequena atualização faz alterações em um ou mais arquivos de aplicativo que são muito menores para garantir a alteração do código do produto.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Pequenas atualizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089982"
---
# <a name="small-updates"></a>Pequenas atualizações

Uma pequena atualização faz alterações em um ou mais arquivos de aplicativo que são muito menores para garantir a alteração do código do produto. Uma pequena atualização também é conhecida como atualização de QFE (rápida correção de engenharia). Uma pequena atualização não permite a reorganização da árvore de componentes de recursos.

Uma pequena atualização típica altera apenas um ou dois arquivos ou uma chave do registro. Como uma pequena atualização altera as informações no arquivo. msi, o código do pacote de instalação deve ser alterado. O código do pacote é armazenado na propriedade [**Resumo do número de revisão**](revision-number-summary.md) do fluxo de informações de [Resumo](summary-information-stream.md).

O código do produto nunca é alterado com uma pequena atualização, portanto, todas as alterações introduzidas por uma pequena atualização precisam ser consistentes com as diretrizes descritas em [alterando o código do produto](changing-the-product-code.md). Uma atualização requer uma [atualização importante](major-upgrades.md) para alterar o [**ProductCode**](productcode.md). Se for necessário diferenciar os produtos sem alterar o código do produto, use uma [atualização secundária](minor-upgrades.md).

Para obter informações sobre como aplicar um pacote de patch de atualização pequena a um pacote Windows Installer, consulte [criando um patch de atualização pequeno](creating-a-small-update-patch.md), [aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [aplicando pequenas atualizações reinstalando o produto](applying-small-updates-by-reinstalling-the-product.md)e [aplicando pequenas atualizações por meio de patch de uma imagem administrativa](applying-small-updates-by-patching-an-administrative-image.md).

 

 



