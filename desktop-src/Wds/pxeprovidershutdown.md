---
title: Função de retorno de chamada PxeProviderShutdown
description: Chamado para desligar o provedor.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Função de retorno de chamada do PxeProviderShutdown serviços de implantação do Windows
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762372"
---
# <a name="pxeprovidershutdown-callback-function"></a>Função de retorno de chamada PxeProviderShutdown

Chamado para desligar o provedor. Essa função é registrada chamando a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) com o parâmetro *CallbackType* definido como **\_ \_ desligamento de retorno de chamada PXE**. Depois que essa função é chamada, o identificador *hProvider* passado para a função [*PxeProviderInitialize*](pxeproviderinitialize.md) não é mais válido.

## <a name="syntax"></a>Sintaxe


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContext* \[ no\]
</dt> <dd>

Valor de contexto passado para a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o provedor for desligado com êxito, o retorno de chamada deverá retornar o **erro de \_ êxito**. Em caso de falha, um código de erro apropriado deve ser retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008, Windows Server 2003 com aplicativos de área de trabalho do SP2 \[ somente\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de servidor dos serviços de implantação do Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderInitialize*](pxeproviderinitialize.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





