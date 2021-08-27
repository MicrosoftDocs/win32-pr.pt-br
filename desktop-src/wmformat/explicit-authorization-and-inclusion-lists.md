---
title: Autorização explícita e listas de inclusão
description: Autorização explícita e listas de inclusão
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows SDK de formato de mídia, exportação de DRM
- Windows Media Format SDK, exportar
- Windows SDK do formato de mídia, autorização explícita e listas de inclusão
- Windows SDK do formato de mídia, listas de autorização
- Windows SDK do formato de mídia, listas de inclusão
- DRM (gerenciamento de direitos digitais), exportar
- DRM (gerenciamento de direitos digitais), exportar
- DRM (gerenciamento de direitos digitais), autorização explícita e listas de inclusão
- DRM (gerenciamento de direitos digitais), autorização explícita e listas de inclusão
- DRM (gerenciamento de direitos digitais), listas de autorização
- DRM (gerenciamento de direitos digitais), listas de autorização
- DRM (gerenciamento de direitos digitais), listas de inclusão
- DRM (gerenciamento de direitos digitais), listas de inclusão
- APIs estendidas do cliente DRM, autorização explícita e listas de inclusão
- APIs estendidas do cliente, autorização explícita e listas de inclusão
- APIs estendidas do cliente DRM, listas de autorização
- APIs estendidas do cliente, listas de autorização
- APIs estendidas do cliente DRM, listas de inclusão
- APIs estendidas do cliente, listas de inclusão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee489d91002cacf7d8a0c89ffeef1752cd844aa089fabbe636e5e50fc185a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089726"
---
# <a name="explicit-authorization-and-inclusion-lists"></a>Autorização explícita e listas de inclusão

as licenças podem conter uma lista de inclusão para autorizar explicitamente a exportação de conteúdo protegido por Windows mídia DRM para outros esquemas de proteção de conteúdo (CPS). De acordo com os termos do contrato de licença que você insere com a Microsoft para habilitar a exportação de DRM, você pode exportar apenas para um CPS válido identificado na lista de inclusão de uma licença.

Uma lista de inclusão é uma matriz vinculada de GUIDs (identificadores globais exclusivos) que cada uma representa um determinado CPS autorizado para o qual o conteúdo pode ser exportado. Os GUIDs listados em uma lista de inclusão são independentes dos níveis de proteção de saída (OPL) e dos níveis de proteção de conteúdo (CPL). Impor essas restrições é de responsabilidade do seu aplicativo.

> [!Note]  
> ao executar Windows exportação de DRM de mídia no conteúdo compactado, você acessa a lista de inclusão por meio do método [**IWMDRMLicense:: inclusionlist**](iwmdrmlicense-getinclusionlist.md) . ao executar Windows exportação de DRM de mídia em conteúdo descompactado, use o método [**IWMDRMReader3:: inclusionlist**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) .

 

para registrar um novo sistema de proteção de conteúdo como um Windows mídia drm permitido exportar nas regras de conformidade de exportação do drm de mídia Windows, entre em contato com wmla@microsoft.com .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exportação de DRM**](drm-export.md)
</dt> </dl>

 

 




