---
description: Uma pequena atualização faz alterações em um ou mais arquivos de aplicativo que são muito pequenos para justificar a alteração do código do produto.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Atualizações pequenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 392e19507ca37cf865fab44485b93346dd1ad6cf6d81ada212acb2ec11ddb1c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628166"
---
# <a name="small-updates"></a>Atualizações pequenas

Uma pequena atualização faz alterações em um ou mais arquivos de aplicativo que são muito pequenos para justificar a alteração do código do produto. Uma pequena atualização também é conhecida como uma atualização QFE (engenharia de correção rápida). Uma pequena atualização não permite a reorganização da árvore de componentes de recurso.

Uma atualização pequena típica altera apenas um ou dois arquivos ou uma chave do Registro. Como uma pequena atualização altera as informações no arquivo .msi, o código do pacote de instalação deve ser alterado. O código do pacote é armazenado na propriedade Resumo do Número [**de Revisão**](revision-number-summary.md) do Fluxo de Informações de [Resumo](summary-information-stream.md).

O código do produto nunca é alterado com uma pequena atualização, portanto, todas as alterações introduzidas por uma pequena atualização devem ser consistentes com as diretrizes descritas em Alterando o [código do produto](changing-the-product-code.md). Uma atualização requer uma [atualização principal para](major-upgrades.md) alterar o [**ProductCode.**](productcode.md) Se for necessário diferenciar entre produtos sem alterar o código do produto, use uma [atualização secundária](minor-upgrades.md).

Para obter informações sobre como aplicar um pequeno pacote de patch de atualização a um pacote do instalador do Windows, consulte Criando um patch de atualização [pequeno,](creating-a-small-update-patch.md)aplicando pequenas atualizações aplicando a instalação [local](applying-small-updates-by-patching-the-local-installation-of-the-product.md)do produto , aplicando pequenas atualizações [reinstalando](applying-small-updates-by-reinstalling-the-product.md)o produto e Aplicando pequenas atualizações aplicando uma imagem [administrativa.](applying-small-updates-by-patching-an-administrative-image.md)

 

 



