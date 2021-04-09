---
description: Destrói um objeto de dispositivo do Microsoft DirectDraw no modo de kernel criado anteriormente.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: Função NtGdiDdDeleteDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 9ac10798f83fe7e1a07a0803dd29cfa9cd8b1c98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088917"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a>Função NtGdiDdDeleteDirectDrawObject

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Destrói um objeto de dispositivo do Microsoft DirectDraw no modo de kernel criado anteriormente.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDrawLocal* 
</dt> <dd>

Identificador para o objeto de dispositivo do DirectDraw no modo kernel.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedida, essa função retornará **true**; caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Os aplicativos são aconselhados a usar as APIs do DirectDraw e do [Direct3D](../direct3d10/d3d10-graphics-reference.md) para criar e gerenciar objetos de dispositivo de gráficos. Essas construções abstraem o processo de criação de dispositivos de maneira simplificada e independente do sistema operacional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[**DdDeleteDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
