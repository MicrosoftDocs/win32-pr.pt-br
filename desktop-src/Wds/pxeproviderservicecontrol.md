---
title: Função de retorno de chamada PxeProviderServiceControl
description: Chamado quando um código de controle de serviço é recebido pelo serviço WDS.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Função de retorno de chamada do PxeProviderServiceControl serviços de implantação do Windows
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105814068"
---
# <a name="pxeproviderservicecontrol-callback-function"></a>Função de retorno de chamada PxeProviderServiceControl

Chamado quando um código de controle de serviço é recebido pelo serviço WDS. Essa função de retorno de chamada é registrada chamando a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) com o parâmetro *CallbackType* definido como **\_ controle de serviço de retorno de chamada \_ \_ PXE**.

## <a name="syntax"></a>Sintaxe


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContext* \[ no\]
</dt> <dd>

Valor de contexto passado para a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> <dt>

*dwControl* 
</dt> <dd>

Código de controle. Para obter a lista de valores possíveis, consulte o parâmetro *dwControl* da função [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) .

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

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

