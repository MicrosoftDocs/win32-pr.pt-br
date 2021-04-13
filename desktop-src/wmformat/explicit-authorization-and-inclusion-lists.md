---
title: Autorização explícita e listas de inclusão
description: Autorização explícita e listas de inclusão
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- SDK do Windows Media Format, exportação de DRM
- SDK do Windows Media Format, exportar
- SDK do Windows Media Format, autorização explícita e listas de inclusão
- SDK do Windows Media Format, listas de autorização
- SDK do Windows Media Format, listas de inclusão
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
ms.openlocfilehash: 2309bed28ffd3add2a75c1cd90488b9ef454659b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365547"
---
# <a name="explicit-authorization-and-inclusion-lists"></a>Autorização explícita e listas de inclusão

As licenças podem conter uma lista de inclusão para autorizar explicitamente a exportação de conteúdo protegido pelo Windows Media DRM para outros esquemas de proteção de conteúdo (CPS). De acordo com os termos do contrato de licença que você insere com a Microsoft para habilitar a exportação de DRM, você pode exportar apenas para um CPS válido identificado na lista de inclusão de uma licença.

Uma lista de inclusão é uma matriz vinculada de GUIDs (identificadores globais exclusivos) que cada uma representa um determinado CPS autorizado para o qual o conteúdo pode ser exportado. Os GUIDs listados em uma lista de inclusão são independentes dos níveis de proteção de saída (OPL) e dos níveis de proteção de conteúdo (CPL). Impor essas restrições é de responsabilidade do seu aplicativo.

> [!Note]  
> Ao executar a exportação do DRM do Windows Media no conteúdo compactado, você acessa a lista de inclusão por meio do método [**IWMDRMLicense:: inclusionlist**](iwmdrmlicense-getinclusionlist.md) . Ao executar a exportação do DRM do Windows Media em conteúdo descompactado, use o método [**IWMDRMReader3:: inclusionlist**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) .

 

Para registrar um novo sistema de proteção de conteúdo como uma exportação do DRM do Windows Media em regras de conformidade de exportação do Windows Media DRM, entre em contato com wmla@microsoft.com .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exportação de DRM**](drm-export.md)
</dt> </dl>

 

 




