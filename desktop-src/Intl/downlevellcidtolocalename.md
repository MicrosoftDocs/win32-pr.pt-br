---
description: Converte um identificador de localidade em um nome de localidade.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: Função DownlevelLCIDToLocaleName (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b96d0c983c46c5d16007aae3a59659099a48855048194153d0c8102d26dc5bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898716"
---
# <a name="downlevellcidtolocalename-function"></a>Função DownlevelLCIDToLocaleName

Converte um [identificador de localidade](locale-identifiers.md) em um [nome de localidade](locale-names.md).

> [!Note]  
> essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista. Seu uso requer um pacote de download. os aplicativos que são executados somente no Windows Vista e posterior devem chamar [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) para recuperar um nome de localidade.

 

## <a name="syntax"></a>Sintaxe


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localidade* \[ do no\]
</dt> <dd>

O identificador de localidade a ser convertido. Você pode usar a macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para criar um identificador de localidade. Esta função não oferece suporte a localidades neutras ou a valores de identificador de localidade específicos a seguir.

-   [\_padrão do sistema de localidade \_](locale-system-default.md)
-   [\_padrão de usuário de localidade \_](locale-user-default.md)
-   [\_padrão personalizado de localidade \_](locale-custom-constants.md)
-   [\_ \_ padrão da interface do usuário personalizada de localidade \_](locale-custom-constants.md)
-   [LOCALIDADE \_ personalizada \_ não especificada](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual essa função recupera o nome da localidade. A função recupera **NULL** se *cchName* estiver definido como 0.

</dd> <dt>

*cchName* \[ no\]
</dt> <dd>

Tamanho, em pontos de código UTF-16, do buffer de nome de localidade. O aplicativo define esse parâmetro como 0 para retornar o tamanho necessário do buffer de nome de localidade.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Sinalizadores que especificam o tipo de nome a recuperar. O valor padrão é nome de localidade de nível inferior \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a contagem de pontos de código UTF-16 no nome da localidade, incluindo o caractere nulo de terminação, se for bem-sucedido. Se a função for bem sucedido e o valor de *cchName* for 0, o valor de retorno será o tamanho necessário, em caracteres (incluindo caracteres nulos), para o buffer de nome de localidade.

A função retornará 0 se não tiver sucesso. Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   ERRO \_ de \_ buffer insuficiente. Um tamanho de buffer fornecido não era grande o suficiente ou foi definido incorretamente como **nulo**.
-   ERROS de \_ Sinalizadores inválidos \_ . O valor de *dwFlags* não é válido.
-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa função não oferece suporte a [localidades personalizadas](custom-locales.md).

 

O arquivo de cabeçalho e a DLL necessários fazem parte do download "APIs de mapeamento de dados de nível inferior do Microsoft NLS", disponível no [centro de download da Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                |
| Redistribuível<br/>          | APIs de mapeamento de dados de nível inferior do Microsoft NLS onwindows XP com SP2 e laterorWindows vista<br/> |
| Cabeçalho<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao idioma nacional](national-language-support.md)
</dt> <dt>

[Funções de suporte ao idioma nacional](national-language-support-functions.md)
</dt> <dt>

[Mapeando dados de localidade](mapping-locale-data.md)
</dt> <dt>

[**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
