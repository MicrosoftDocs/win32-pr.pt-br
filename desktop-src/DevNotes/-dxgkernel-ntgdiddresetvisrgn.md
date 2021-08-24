---
description: Usado para permitir que o modo de usuário obtenha uma compreensão válida da região de recorte para janelas na área de trabalho. Esse recorte pode mudar de forma assíncrona do ponto de vista dos threads de modo de usuário.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Função NtGdiDdResetVisrgn (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 3077351b804f854520cff421fcad8a575278bb5a960f60ef760db38e7ca2f3a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833636"
---
# <a name="ntgdiddresetvisrgn-function"></a>Função NtGdiDdResetVisrgn

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Usado para permitir que o modo de usuário obtenha uma compreensão válida da região de recorte para janelas na área de trabalho. Esse recorte pode mudar de forma assíncrona do ponto de vista dos threads de modo de usuário.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurface* \[ Em\]
</dt> <dd>

Ponteiro para o objeto de modo de usuário de qualquer superfície pertencente ao dispositivo DirectDraw para o qual o recorte deve ser redefinido. Para obter detalhes, consulte a documentação do DDK.

</dd> <dt>

*hwnd* \[ Em\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedida, essa função **retornará TRUE;** caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

O recorte pode mudar de forma assíncrona do ponto de vista dos threads de modo de usuário. As partes de modo kernel do DirectDraw e Windows Graphics Device Interface (GDI) mantêm um contador que é incrementado sempre que a lista de recortes de toda a área de trabalho é muda. Uma chamada para essa função registra esse contador com todas as superfícies primárias do DirectDraw existentes no sistema.

A qualquer momento posterior, quando uma dessas superfícies primárias for modificada por uma operação [IDirectDrawSurface7::Blt](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) ou [IDirectDrawSurface7::Lock](/previous-versions/ms858221(v=msdn.10)) (consulte a documentação do DDK), o contador registrado com a superfície será comparado com o contador global. Se esses valores são diferentes, um código de erro CHANGR \_ VISRGNCHANGED é retornado para o código de modo de usuário. Em seguida, o código de modo de usuário consultará novamente o recorte atual para a área de trabalho, chamará **NtGdiDdResetVisrgn** e tentará novamente o IDirectDrawSurface7::Blt aplicado à superfície primária, respeitando o novo recorte. Por fim, o recorte que foi amostrado pelo código de modo de usuário será o mesmo que o recorte atual pertencente ao modo kernel e O IDirectDrawSurface7::Blt terá permissão para continuar.

Os aplicativos são aconselhados a usar a interface [IDirectDrawClipper](/previous-versions/aa919448(v=msdn.10)) ou o método [IDirect3DDevice8::P resent](/previous-versions/ms889707(v=msdn.10)) para lidar com alterações de recorte assíncronas. Esses constructos implementam o recorte assíncrono de maneira automatizada e independente do sistema operacional.

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

[**DdResetVisrgn**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
