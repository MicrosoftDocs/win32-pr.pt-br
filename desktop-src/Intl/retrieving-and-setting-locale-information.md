---
description: Recuperando e definindo informações de localidade
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Recuperando e definindo informações de localidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d02c2bb58328529781309ce8284310acbcb6fb545ecdc076df295cd020344a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130306"
---
# <a name="retrieving-and-setting-locale-information"></a>Recuperando e definindo informações de localidade

O aplicativo deve ser capaz de recuperar e definir informações específicas sobre [localidades e idiomas](locales-and-languages.md)disponíveis. Cada elemento de informações de localidade, como o nome de um dia específico da semana ou o caractere usado como separador decimal, tem uma constante correspondente. As constantes disponíveis são definidas nas [constantes de informações de localidade](locale-information-constants.md).

Seu aplicativo sempre armazena e manipula informações de localidade como uma cadeia de caracteres terminada em nulo. Nenhum dado binário é permitido e todos os valores numéricos devem ser especificados como texto. Cada tipo de informação tem um formato específico. Além disso, vários tipos são vinculados para que a alteração de um tipo também altere o valor do outro tipo.

Para recuperar informações de localidade, o aplicativo chama [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) com a constante que corresponde às informações necessárias. O aplicativo pode chamar [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) para definir um item de informações de localidade.

> [!Note]  
> Embora um [identificador de localidade](locale-identifiers.md) possa ter suporte, ele não estará disponível para uso por um aplicativo, a menos que a localidade correspondente também esteja instalada.

 

Como a maioria das constantes de informações de localidade é mutuamente exclusiva, apenas um tipo de informação pode ser manipulado de cada vez. As exceções a essa regra são a [localidade \_ usar \_ CP \_ ACP](locale-use-cp-acp.md), [ \_ \_ número de retorno de localidade](locale-return-constants.md)e [ \_ NOUSEROVERRIDE de localidade](locale-nouseroverride.md), que podem ser combinados com outras constantes usando um binário ou.

> [!Caution]  
> O uso de \_ NOUSEROVERRIDE de localidade é fortemente desencorajado, pois desabilita as preferências do usuário.

 

Como uma série de aplicativos, por exemplo, o Microsoft Active Directory, seu aplicativo pode manter suas cadeias de caracteres em um banco de dados classificável. Para obter mais informações, consulte [lidando com a classificação em seus aplicativos](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o suporte ao idioma nacional](using-national-language-support.md)
</dt> <dt>

[Constantes de informações de localidade](locale-information-constants.md)
</dt> <dt>

[Lidando com a classificação em seus aplicativos](handling-sorting-in-your-applications.md)
</dt> <dt>

[Trabalhando com localidades personalizadas](working-with-custom-locales.md)
</dt> </dl>

 

 



