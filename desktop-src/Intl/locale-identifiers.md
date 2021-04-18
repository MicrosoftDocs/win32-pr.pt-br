---
description: Cada localidade tem um identificador exclusivo, um valor de 32 bits que consiste em um identificador de idioma e um identificador de ordem de classificação.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Identificadores de localidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767631"
---
# <a name="locale-identifiers"></a>Identificadores de localidade

Cada [localidade](locales-and-languages.md) tem um identificador exclusivo, um valor de 32 bits que consiste em um [identificador de idioma](language-identifiers.md) e um [identificador de ordem de classificação](sort-order-identifiers.md). O identificador de localidade é uma abreviação numérica internacional padrão e tem os componentes necessários para identificar exclusivamente uma das localidades definidas pelo sistema operacional instaladas. O NLS dá suporte a identificadores de localidade predefinidos e identificadores personalizados.

> [!Note]  
> Os nomes de localidade podem ser usados com funções introduzidas no Windows Vista que usam um [nome de localidade](locale-names.md) como parâmetro, em vez de um identificador de localidade. Para obter mais informações, consulte [chamar as funções de "nome de localidade"](calling-the--locale-name--functions.md). O uso de nomes de localidade em vez de identificadores de localidade é sempre preferível.

 

A ilustração a seguir mostra o formato dos bits em um identificador de localidade.

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a>Identificadores de localidade predefinidos

Os identificadores de localidade predefinidos com suporte pelo NLS são definidos na [referência da API NLS (suporte ao idioma nacional)](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

O NLS usa as seguintes constantes de informações de localidade para representar identificadores de localidade.

-   [Localidade \_ do SLANGUAGE](locale-slanguage.md) ou [localidade \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)
-   [SNAME de localidade \_](locale-sname.md)
-   [SSCRIPTS de localidade \_](locale-sscripts.md)
-   [IDEFAULTANSICODEPAGE de localidade \_](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a>Identificadores de localidade personalizados

**Windows Vista:** O NLS dá suporte aos identificadores de localidade personalizados representados pelas seguintes constantes de informações de localidade.

-   [\_padrão personalizado de localidade \_](locale-custom-constants.md)
-   [\_ \_ padrão da interface do usuário personalizada de localidade \_](locale-custom-constants.md)
-   [LOCALIDADE \_ personalizada \_ não especificada](locale-custom-constants.md)

## <a name="building-a-locale"></a>Criando uma localidade

Você pode usar o utilitário do Locale Builder fornecido pelo NLS para criar localidades. Para obter mais informações, consulte [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).

Seu aplicativo pode construir um identificador de localidade usando a macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) . Como alternativa, ele pode usar um dos identificadores padrão correspondentes às constantes listadas abaixo.

-   [LOCALIDADE \_ invariável](locale-invariant.md)
-   [\_padrão do sistema de localidade \_](locale-system-default.md)
-   [\_padrão de usuário de localidade \_](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a>Recuperação de identificadores de localidade

Um aplicativo pode recuperar os identificadores de localidade atuais usando as funções [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) e [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) . Cada thread pode definir e recuperar sua própria localidade com [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) e [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localidades e idiomas](locales-and-languages.md)
</dt> <dt>

[Identificadores de idioma](language-identifiers.md)
</dt> <dt>

[Nomes de localidade](locale-names.md)
</dt> <dt>

[Identificadores de ordem de classificação](sort-order-identifiers.md)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
