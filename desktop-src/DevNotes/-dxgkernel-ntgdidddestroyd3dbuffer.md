---
description: Destrói um objeto de superfície do Microsoft DirectDraw no modo kernel alocado anteriormente que foi criado com o membro dwCaps da estrutura DDSCAPS definido como DDSCAPS \_ EXECUTEBUFFER.
ms.assetid: c737b706-25be-49b8-8d8c-35f48aea2889
title: Função NtGdiDdDestroyD3DBuffer (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c1cd9ba5822d823f3353bd1a33040c5449e97727389e5a7407b409aa475c8dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956515"
---
# <a name="ntgdidddestroyd3dbuffer-function"></a>Função NtGdiDdDestroyD3DBuffer

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Destrói um objeto de superfície do Microsoft DirectDraw no modo kernel alocado anteriormente que foi criado com o membro **dwCaps** da estrutura [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) definido como DDSCAPS \_ EXECUTEBUFFER.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdDestroyD3DBuffer(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurface* \[ Em\]
</dt> <dd>

Lidar com uma [**estrutura DD \_ DESTROYSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) que contém as informações necessárias para destruir um comando Direct3D ou buffer de vértice.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdDestroyD3DBuffer** retorna um dos códigos de retorno de chamada a seguir.



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

 

 
