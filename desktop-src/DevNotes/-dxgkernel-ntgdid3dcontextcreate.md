---
description: Cria um contexto.
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: Função NtGdiD3DContextCreate (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextCreate
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: a11ae1d1e9b9469f22971ec3fc7447d8552b6d263bb43f4a8fe336ccbbc37a69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017734"
---
# <a name="ntgdid3dcontextcreate-function"></a>Função NtGdiD3DContextCreate

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Cria um contexto.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDrawLocal* \[ Em\]
</dt> <dd>

Identificador para um objeto DirectDraw no modo kernel, criado anteriormente com [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), representando o dispositivo no qual o contexto direct3D deve ser criado.

</dd> <dt>

*hSurfColor* \[ Em\]
</dt> <dd>

Lidar com uma [**estrutura LOCAL do DD \_ SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície do DirectDraw a ser usada como o destino de renderização.

</dd> <dt>

*hSurfZ* \[ Em\]
</dt> <dd>

Lidar com uma [**estrutura LOCAL do DD \_ SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície do DirectDraw a ser usada como um buffer de profundidade. Se esse membro for **NULL,** nenhum buffer de profundidade será executado.

</dd> <dt>

*pdcci* \[ in, out\]
</dt> <dd>

Ponteiro para uma [**estrutura D3DNTHAL \_ CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) que contém as informações necessárias para criar um contexto e os dados que o driver deve armazenar no novo contexto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiD3DContextCreate** retorna um dos seguintes códigos de retorno de chamada.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ MANIPULADO**</dt> </dl>    | O driver realizou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, DirectDraw ou Direct3D prosseguirá com a função . Caso contrário, DirectDraw ou Direct3D retornará o código de erro fornecido pelo driver e anulará a função.<br/>                                                                                 |
| <dl> <dt>**DDHAL \_ DRIVER \_ NOTHANDLED**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se o driver precisar ter implementado um retorno de chamada específico, DirectDraw ou Direct3D relata uma condição de erro. Caso contrário, DirectDraw ou Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido executando a implementação independente de dispositivo DirectDraw ou Direct3D.<br/> |



 

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

 

 
