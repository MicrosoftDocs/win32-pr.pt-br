---
title: Função de retorno de chamada PxeProviderInitialize
description: Uma exportação de uma DLL (biblioteca de vínculo dinâmico) do provedor que inicializa o provedor e o prepara para receber solicitações do cliente.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Função de retorno de chamada PxeProviderInitialize Windows Deployment Services
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6eb7ba32049dc3ef70085a489b499d90b92ec6155323b650df0e2b2f839bbdf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098656"
---
# <a name="pxeproviderinitialize-callback-function"></a>Função de retorno de chamada PxeProviderInitialize

Uma exportação de uma DLL (biblioteca de vínculo dinâmico) do provedor que inicializa o provedor e o prepara para receber solicitações do cliente. Os provedores são necessários para exportar a *função PxeProviderInitialize.* Todos os retornos de chamada para o provedor devem ser registrados com uma chamada para a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) durante o processamento de *PxeProviderInitialize*. No retorno dessa função, o provedor deve ser totalmente inicializado e pronto para processar solicitações do cliente.

## <a name="syntax"></a>Sintaxe


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProvider* \[ Em\]
</dt> <dd>

Lidar com a instância do provedor. Esse handle deve ser armazenado pelo provedor e usado em quaisquer chamadas subsequentes. Esse handle é válido até que a função de retorno de chamada [*PxeProviderShutdown*](pxeprovidershutdown.md) seja chamada.

</dd> <dt>

*hProviderKey* \[ Em\]
</dt> <dd>

Lidar com uma chave do Registro em que as informações de configuração do provedor devem ser armazenadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a inicialização do provedor for bem-sucedida, o retorno de chamada deverá retornar **ERROR \_ SUCCESS**. Em caso de falha, um código de erro apropriado deve ser retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008, Windows Server 2003 somente com aplicativos da área de trabalho SP2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Windows Funções de servidor dos Serviços de Implantação](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderShutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 





