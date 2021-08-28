---
description: Para NLS, a classificação (também conhecida como &\# 0034;ordenação&\# 0034;) é a organização de cadeias de caracteres.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Classificação (internacionalização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3dbedf872c953a45ca7064eccd4ba16019a857c35186261695e094be03cd054
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130206"
---
# <a name="sorting"></a>Classificação

Para NLS, a classificação (também conhecida como "ordenação") é a organização de cadeias de caracteres. Há dois tipos de classificação:

-   Classificação linguística. Organiza cadeias de caracteres com características linguísticas semelhantes em grupos (por classificações).
-   Classificação ordinal (não linguística). Organiza as cadeias de caracteres em uma sequência ordenada.

A classificação usa as funções de comparação de cadeia de caracteres NLS, como [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)ou funções de API "wrapper", como [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), que chamam internamente as funções de comparação de cadeia de caracteres NLS.

Para obter detalhes sobre como implementar a classificação em seus aplicativos, consulte [Manipulando a classificação em seus aplicativos.](handling-sorting-in-your-applications.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o suporte a idiomas nacionais](about-national-language-support.md)
</dt> <dt>

[Manipulando a classificação em seus aplicativos](handling-sorting-in-your-applications.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[Lcmapstring](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
