---
description: Permite que o driver informe que aloca internamente a memória de exibição para executar a compensação de movimento.
ms.assetid: cf2878ae-7eff-4214-bb9e-e8b608831108
title: Função NtGdiDdGetInternalMoCompInfo (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetInternalMoCompInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 323c6d36284032f5d9fb1ee73b90393ed3d00c0c8247002c1f8b0f42484784fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103856"
---
# <a name="ntgdiddgetinternalmocompinfo-function"></a>Função NtGdiDdGetInternalMoCompInfo

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Permite que o driver informe que aloca internamente a memória de exibição para executar a compensação de movimento.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdGetInternalMoCompInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETINTERNALMOCOMPDATA puGetInternalData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDraw* \[ Em\]
</dt> <dd>

Identificador para o objeto DirectDraw no modo kernel criado anteriormente.

</dd> <dt>

*puGetInternalData* \[ in, out\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ GETINTERNALMOCOMPDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getinternalmocompdata) que contém os requisitos de memória interna.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdGetInternalMoCompInfo** retorna um dos códigos de retorno de chamada a seguir.



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

 

 
