---
description: A tabela UpgradedFilesToIgnore impede a atualização de arquivos específicos que, na verdade, são alterados na imagem atualizada em relação às imagens de destino.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Tabela UpgradedFilesToIgnore (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51143fcf7db350d5ee8aa1e43d49984914bcf9f05a2f8f5f787834a69b7e1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809546"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a>Tabela UpgradedFilesToIgnore (Patchwiz.dll)

A tabela UpgradedFilesToIgnore impede a atualização de arquivos específicos que, na verdade, são alterados na imagem atualizada em relação às imagens de destino. Pode ser útil fazer isso em determinados casos. Por exemplo, um pacote de patches destinado apenas ao uso com instalações não administrativas não precisa incluir arquivos de patch que sejam apenas parte das imagens administrativas. Excluir esses arquivos usados somente em imagens administrativas pode reduzir o tamanho do pacote de patches; no entanto, os administradores devem ser informados sobre como atualizar esses arquivos separadamente. Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

A tabela UpgradedFilesToIgnore tem as colunas a seguir.



| Coluna   | Tipo | Chave | Nullable |
|----------|------|-----|----------|
| Atualizado | texto | Y   | N        |
| FTK      | texto | Y   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Foram
</dt> <dd>

Chave estrangeira para a coluna atualizada da [tabela UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md). A ferramenta de criação de patch exclui a atualização do arquivo especificado na coluna FTK da tabela UpgradedFilesToIgnore ao atualizar um destino para a imagem especificada no campo atualizado. Insira um valor de " \* " no campo atualizado para excluir a atualização do arquivo para todas as imagens atualizadas.

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chave estrangeira na [tabela de arquivos](file-table.md) da imagem atualizada. Um valor da forma " <prefix> \* " corresponde a todas as chaves de tabela de arquivos na tabela de arquivos que começam com esse prefixo. Nenhum texto pode seguir o asterisco.

</dd> </dl>

 

 



