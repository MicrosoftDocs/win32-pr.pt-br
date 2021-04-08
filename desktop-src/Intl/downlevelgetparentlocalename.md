---
description: Recupera o nome da localidade para o pai da localidade fornecida.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Função DownlevelGetParentLocaleName (nlsdl. h)
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
ms.openlocfilehash: d3a556d68c33249d2e6b49c48035cc58d8bac8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922549"
---
# <a name="downlevelgetparentlocalename-function"></a>Função DownlevelGetParentLocaleName

Recupera o [nome da localidade](locale-names.md) para o pai da localidade fornecida.

> [!Note]  
> Essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista. Seu uso requer o pacote de download. Os aplicativos que só são executados no Windows Vista e posterior devem chamar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) com *LCTYPE* definido como [localidade \_ SPARENT](locale-sparent.md).

 

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

*Localidade* \[ do no\]
</dt> <dd>

[Identificador de localidade](locale-identifiers.md) da localidade. Você pode usar a macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para criar um identificador de localidade ou usar um dos valores predefinidos a seguir.

-   [LOCALIDADE \_ invariável](locale-invariant.md)
-   [\_padrão do sistema de localidade \_](locale-system-default.md)
-   [\_padrão de usuário de localidade \_](locale-user-default.md)

**Windows Vista e posterior:** Também há suporte para os seguintes identificadores de localidade personalizados.

-   [\_padrão personalizado de localidade \_](locale-custom-constants.md)
-   [\_ \_ padrão da interface do usuário personalizada de localidade \_](locale-custom-constants.md)
-   [LOCALIDADE \_ personalizada \_ não especificada](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual a função recupera o nome da localidade pai ou um dos valores predefinidos a seguir. Esse parâmetro será definido como **NULL** se *cchName* for definido como 0.

-   [nome da localidade \_ \_ invariável](locale-name-constants.md)
-   [nome da localidade \_ \_ padrão do sistema \_](locale-name-constants.md)
-   [nome da localidade \_ \_ usuário \_ padrão](locale-name-constants.md)

</dd> <dt>

*cchName* \[ no\]
</dt> <dd>

Tamanho do buffer indicado por *lpName*, em pontos de código UTF-16. Um valor de 0 para esse parâmetro faz com que a função ignore o buffer *lpName* e retorne o tamanho do buffer, em caracteres (caracteres nulos incluídos), necessário para conter o nome da localidade pai.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a contagem de pontos de código UTF-16 no nome da localidade, incluindo o caractere nulo de terminação, se for bem-sucedido.

Essa função retornará 0 se não tiver sucesso. Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   ERRO \_ de \_ buffer insuficiente. Um tamanho de buffer fornecido não era grande o suficiente ou foi definido incorretamente como **nulo**.
-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

O arquivo de cabeçalho e a DLL necessários fazem parte do download "APIs de mapeamento de dados de nível inferior do Microsoft NLS", disponível no [centro de download da Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Redistribuível<br/>          | APIs de mapeamento de dados de nível inferior do Microsoft NLS no Windows XP com SP2 e posterior<br/>  |
| parâmetro<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao idioma nacional](national-language-support.md)
</dt> <dt>

[Funções de suporte ao idioma nacional](national-language-support-functions.md)
</dt> <dt>

[Mapeando dados de localidade](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
