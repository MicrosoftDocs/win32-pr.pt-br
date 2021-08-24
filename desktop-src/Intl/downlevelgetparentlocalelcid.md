---
description: Recupera o identificador de localidade para o pai da localidade fornecida.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Função DownlevelGetParentLocaleLCID (Nlsdl.h)
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
ms.openlocfilehash: 64cefdf4cc2a2c522a8295ab44e1810f0364d706d378979637700a7a3b72343a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765436"
---
# <a name="downlevelgetparentlocalelcid-function"></a>Função DownlevelGetParentLocaleLCID

Recupera o [identificador de localidade](locale-identifiers.md) para o pai da localidade fornecida.

> [!Note]  
> Essa função é usada somente por aplicativos que são executados em sistemas operacionais Windows Vista pré-executados. Seu uso requer o pacote de download. Os aplicativos que são executados Windows Vista e posterior devem chamar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) com *LCType* definido como [LOCALE \_ SPARENT.](locale-sparent.md)

 

## <a name="syntax"></a>Sintaxe


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localidade* \[ Em\]
</dt> <dd>

Identificador de localidade da localidade para a qual recuperar o identificador de localidade pai. Você pode usar a macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) para criar um identificador de localidade ou usar um dos seguintes valores predefinidos.

-   [LOCALE \_ INVARIANT](locale-invariant.md)
-   [LOCALE \_ SYSTEM \_ DEFAULT](locale-system-default.md)
-   [LOCALE \_ USER \_ DEFAULT](locale-user-default.md)

**Windows Vista e posterior:** Também há suporte para os seguintes identificadores de localidade personalizados.

-   [LOCALE \_ CUSTOM \_ DEFAULT](locale-custom-constants.md)
-   [LOCALE \_ CUSTOM \_ UI \_ DEFAULT](locale-custom-constants.md)
-   [LOCALE \_ PERSONALIZADO \_ NÃO ESPECIFICADO](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o identificador de localidade pai se for bem-sucedido ou 0 caso contrário. Para obter informações de erro estendidas, o aplicativo pode [**chamar GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), que pode retornar um dos seguintes códigos de erro:

-   ERRO \_ PARÂMETRO \_ INVÁLIDO. Qualquer um dos valores de parâmetro era inválido.

## <a name="remarks"></a>Comentários

O arquivo de header necessário e a DLL fazem parte do download das "APIs de mapeamento de dados de nível baixo do Microsoft NLS", disponível no Centro [de Download da Microsoft.](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Redistribuível<br/>          | APIs de mapeamento de dados de nível baixo do Microsoft NLS noWindows XPor Windows Vista<br/>     |
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

 

 
