---
description: Permite que o driver especifique quantas superfícies intermediárias são necessárias para dar suporte ao GUID especificado e o tamanho, o local e o formato de cada uma dessas superfícies.
ms.assetid: 1f3207a8-aa6a-47a3-a1d0-19166592eeca
title: Função NtGdiDdGetMoCompBuffInfo (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetMoCompBuffInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4e2d324cf1b0b986845a7fab95c24abb9f44eb4c6024bbba9be101d25e1318a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956325"
---
# <a name="ntgdiddgetmocompbuffinfo-function"></a>Função NtGdiDdGetMoCompBuffInfo

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Permite que o driver especifique quantas superfícies intermediárias são necessárias para dar suporte ao GUID especificado e o tamanho, o local e o formato de cada uma dessas superfícies.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdGetMoCompBuffInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETMOCOMPCOMPBUFFDATA puGetBuffData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDraw* \[ Em\]
</dt> <dd>

Identificador para o objeto DirectDraw no modo kernel criado anteriormente.

</dd> <dt>

*puGetBuffData* \[ in, out\]
</dt> <dd>

Ponteiro para uma [**estrutura DD \_ GETMOCOMPCOMPBUFFDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata) que contém as informações de buffer compactado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdGetMoCompBuffInfo** retorna um dos códigos de retorno de chamada a seguir.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ MANIPULADO**</dt> </dl>    | O driver realizou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, DirectDraw ou Direct3D prosseguirá com a função . Caso contrário, DirectDraw ou Direct3D retornará o código de erro fornecido pelo driver e anulará a função.<br/>                                                                                 |
| <dl> <dt>**DDHAL \_ DRIVER \_ NOTHANDLED**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se o driver precisar ter implementado um retorno de chamada específico, DirectDraw ou Direct3D relata uma condição de erro. Caso contrário, DirectDraw ou Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido executando a implementação independente de dispositivo DirectDraw ou Direct3D.<br/> |



 

## <a name="remarks"></a>Comentários

Para obter mais informações, consulte O DDK (Kit de Desenvolvimento de Driver de Aceleração de Vídeo) do Microsoft DirectX.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
