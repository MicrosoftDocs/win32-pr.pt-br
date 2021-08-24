---
description: Recupera o nome da localidade para o pai da localidade fornecida.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Função DownlevelGetParentLocaleName (Nlsdl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: af7580188c7ded31c80476509aef8a10ee83b1cb1f9767ca5819eed053f1ce87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898736"
---
# <a name="downlevelgetparentlocalename-function"></a>Função DownlevelGetParentLocaleName

Recupera o [nome da localidade](locale-names.md) para o pai da localidade fornecida.

> [!Note]  
> Essa função é usada somente por aplicativos que são executados em sistemas operacionais Windows Vista pré-executados. Seu uso requer o pacote de download. Os aplicativos que são executados Windows Vista e posterior devem chamar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) com *LCType* definido como [LOCALE \_ SPARENT.](locale-sparent.md)

 

## <a name="syntax"></a>Sintaxe


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localidade* \[ Em\]
</dt> <dd>

[Identificador de localidade](locale-identifiers.md) da localidade. Você pode usar a macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para criar um identificador de localidade ou usar um dos seguintes valores predefinidos.

-   [LOCALE \_ INVARIANT](locale-invariant.md)
-   [LOCALE \_ SYSTEM \_ DEFAULT](locale-system-default.md)
-   [LOCALE \_ USER \_ DEFAULT](locale-user-default.md)

**Windows Vista e posterior:** Também há suporte para os seguintes identificadores de localidade personalizados.

-   [LOCALE \_ CUSTOM \_ DEFAULT](locale-custom-constants.md)
-   [LOCALE \_ CUSTOM \_ UI \_ DEFAULT](locale-custom-constants.md)
-   [LOCALE \_ PERSONALIZADO \_ NÃO ESPECIFICADO](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ out\]
</dt> <dd>

Ponteiro para um buffer no qual a função recupera o nome da localidade pai ou um dos seguintes valores predefinidos. Esse parâmetro será definido como **NULL se** *cchName* estiver definido como 0.

-   [LOCALE \_ NAME \_ INVARIANT](locale-name-constants.md)
-   [PADRÃO DO \_ SISTEMA DE NOMES DE \_ \_ LOCALIDADE](locale-name-constants.md)
-   [LOCALE \_ NAME \_ USER \_ DEFAULT](locale-name-constants.md)

</dd> <dt>

*cchName* \[ Em\]
</dt> <dd>

Tamanho do buffer indicado por *lpName*, em pontos de código UTF-16. Um valor de 0 para esse parâmetro faz com que a função ignore o buffer *lpName* e retorne o tamanho do buffer, em caracteres (caracteres nulos incluídos), necessário para conter o nome da localidade pai.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a contagem de pontos de código UTF-16 no nome da localidade, incluindo o caractere nulo de terminação, se bem-sucedido.

Essa função retornará 0 se não tiver êxito. Para obter informações de erro estendidas, o aplicativo pode [**chamar GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   ERRO \_ BUFFER \_ INSUFICIENTE. Um tamanho de buffer fornecido não era grande o suficiente ou foi definido incorretamente como **NULL.**
-   ERRO \_ PARÂMETRO \_ INVÁLIDO. Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

O arquivo de header necessário e a DLL fazem parte do download das "APIs de mapeamento de dados de nível baixo do Microsoft NLS", disponível no Centro [de Download da Microsoft.](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Redistribuível<br/>          | APIs de mapeamento de dados de nível baixo do Microsoft NLS noWindows XP com SP2 e posterior<br/>  |
| Cabeçalho<br/>                   | <dl> <dt>Nlsdl.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte a idiomas nacionais](national-language-support.md)
</dt> <dt>

[Funções de suporte a idiomas nacionais](national-language-support-functions.md)
</dt> <dt>

[Mapeando dados de localidade](mapping-locale-data.md)
</dt> <dt>

[**Getlocaleinfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
