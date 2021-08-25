---
description: Converte um nome de localidade em um identificador de localidade que pode ser usado para obter informações do sistema operacional.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Função DownlevelLocaleNameToLCID (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 39a0a6b274ba141553d2ddda927f71754cc9639ff5fc3a0d3870a974e46526a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898726"
---
# <a name="downlevellocalenametolcid-function"></a>Função DownlevelLocaleNameToLCID

Converte um [nome de localidade](locale-names.md) em um [identificador de localidade](locale-identifiers.md) que pode ser usado para obter informações do sistema operacional.

> [!Note]  
> essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista. Seu uso requer um pacote de download. os aplicativos que só são executados no Windows Vista e posterior devem chamar [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) para recuperar um identificador de localidade.

 

## <a name="syntax"></a>Sintaxe


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpName* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que representa um [nome de localidade](locale-names.md).

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Sinalizadores que especificam o tipo de nome. O padrão é nome de localidade de nível inferior \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o identificador de localidade que corresponde ao nome da localidade, se for bem-sucedido.

A função retornará 0 se não tiver sucesso. Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   ERROS de \_ Sinalizadores inválidos \_ . Os valores fornecidos para sinalizadores não eram válidos.
-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

> [!Note]  
> Esta função não oferece suporte a localidades neutras. a função [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) equivalente dá suporte a [localidades personalizadas](custom-locales.md), mas somente para Windows Vista e posterior.

 

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

[**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
