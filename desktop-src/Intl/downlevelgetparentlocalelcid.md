---
description: Recupera o identificador de localidade para o pai da localidade fornecida.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Função DownlevelGetParentLocaleLCID (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297278"
---
# <a name="downlevelgetparentlocalelcid-function"></a>Função DownlevelGetParentLocaleLCID

Recupera o [identificador de localidade](locale-identifiers.md) para o pai da localidade fornecida.

> [!Note]  
> Essa função é usada somente por aplicativos que são executados em sistemas operacionais anteriores ao Windows Vista. Seu uso requer o pacote de download. Os aplicativos que só são executados no Windows Vista e posterior devem chamar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) com *LCTYPE* definido como [localidade \_ SPARENT](locale-sparent.md).

 

## <a name="syntax"></a>Sintaxe


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localidade* \[ do no\]
</dt> <dd>

Identificador de localidade da localidade para a qual recuperar o identificador de localidade pai. Você pode usar a macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para criar um identificador de localidade ou usar um dos valores predefinidos a seguir.

-   [LOCALIDADE \_ invariável](locale-invariant.md)
-   [\_padrão do sistema de localidade \_](locale-system-default.md)
-   [\_padrão de usuário de localidade \_](locale-user-default.md)

**Windows Vista e posterior:** Também há suporte para os seguintes identificadores de localidade personalizados.

-   [\_padrão personalizado de localidade \_](locale-custom-constants.md)
-   [\_ \_ padrão da interface do usuário personalizada de localidade \_](locale-custom-constants.md)
-   [LOCALIDADE \_ personalizada \_ não especificada](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador de localidade pai se for bem-sucedido ou 0 caso contrário. Para obter informações de erro estendidas, o aplicativo pode chamar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   \_parâmetro inválido de erro \_ . Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

O arquivo de cabeçalho e a DLL necessários fazem parte do download "APIs de mapeamento de dados de nível inferior do Microsoft NLS", disponível no [centro de download da Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Redistribuível<br/>          | APIs de mapeamento de dados de nível inferior do Microsoft NLS onwindows XPor Windows Vista<br/>     |
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

 

 
