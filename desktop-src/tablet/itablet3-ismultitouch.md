---
description: Determina se um dispositivo de entrada dá suporte a multitoque.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: 'Método ITablet3:: IsMultiTouch'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171158"
---
# <a name="itablet3ismultitouch-method"></a>Método ITablet3:: IsMultiTouch

Determina se um dispositivo de entrada dá suporte a multitoque.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bIsMultiTouch* \[ fora\]
</dt> <dd>

Indica se o dispositivo é multitoque.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **S \_ OK** em caso de êxito; caso contrário, retorna um código de erro como **E \_ falha**.

## <a name="remarks"></a>Comentários

Depois de determinar por meio de [**IRealTimeStylus3:: MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) ou **ITablet3:: IsMultiTouch** que multitoque está disponível, um aplicativo pode optar por aceitar as mensagens de entrada de multitoque. Informações adicionais sobre como filtrar métodos multitoque estão disponíveis na seção da propriedade **IRealTimeStylus3:: MultiTouchEnabled** .

## <a name="examples"></a>Exemplos


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> <dt>

[**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




