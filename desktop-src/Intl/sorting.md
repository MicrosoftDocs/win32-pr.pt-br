---
description: Para NLS, classificação (também conhecido como &\# 0034; agrupamento&\# 0034;) é a organização de cadeias de caracteres.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Classificação (internacionalização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172033"
---
# <a name="sorting"></a>Classificação

Para NLS, a classificação (também conhecida como "Agrupamento") é a organização das cadeias de caracteres. Há dois tipos de classificação:

-   Classificação linguística. Organiza cadeias de caracteres com características linguísticas semelhantes em grupos (por classificação).
-   Classificação Ordinal (não lingüística). Organiza as cadeias de caracteres em uma sequência ordenada.

A classificação usa as funções de comparação de cadeia de caracteres NLS, como [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), ou funções de API "wrapper", como [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), que chamam internamente as funções de comparação de cadeia de caracteres NLS.

Para obter detalhes sobre como implementar a classificação em seus aplicativos, consulte [lidando com a classificação em seus aplicativos](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o suporte ao idioma nacional](about-national-language-support.md)
</dt> <dt>

[Lidando com a classificação em seus aplicativos](handling-sorting-in-your-applications.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[LCMapString](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
