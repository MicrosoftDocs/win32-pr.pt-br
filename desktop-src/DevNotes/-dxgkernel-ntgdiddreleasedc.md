---
description: Libera o DC (contexto de dispositivo) criado anteriormente para o objeto de superfície do Microsoft DirectDraw no modo kernel indicado.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: Função NtGdiDdReleaseDC (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: daa4cad2f6f3937ebe29b3996ebbaa72b894ee743f97222cb1f6e2ff61f7dbb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824906"
---
# <a name="ntgdiddreleasedc-function"></a>Função NtGdiDdReleaseDC

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Libera o DC (contexto de dispositivo) criado anteriormente para o objeto de superfície do Microsoft DirectDraw no modo kernel indicado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurface* \[ Em\]
</dt> <dd>

Identificador para o objeto de superfície directDraw do modo kernel criado anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedida, essa função **retornará TRUE;** caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

Os aplicativos que precisam obter um DC para uma superfície do DirectDraw podem usar [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), que expõe essa funcionalidade de maneira independente do sistema operacional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdReleaseDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
