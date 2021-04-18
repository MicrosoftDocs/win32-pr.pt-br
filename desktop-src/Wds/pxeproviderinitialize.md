---
title: Função de retorno de chamada PxeProviderInitialize
description: Uma exportação de uma DLL (biblioteca de vínculo dinâmico) do provedor que inicializa o provedor e a prepara para receber solicitações do cliente.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Função de retorno de chamada do PxeProviderInitialize serviços de implantação do Windows
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796238"
---
# <a name="pxeproviderinitialize-callback-function"></a>Função de retorno de chamada PxeProviderInitialize

Uma exportação de uma DLL (biblioteca de vínculo dinâmico) do provedor que inicializa o provedor e a prepara para receber solicitações do cliente. Os provedores são necessários para exportar a função *PxeProviderInitialize* . Qualquer retorno de chamada para o provedor deve ser registrado com uma chamada para a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) durante o processamento de *PxeProviderInitialize*. No retorno dessa função, o provedor deve ser totalmente inicializado e estar pronto para processar solicitações de cliente.

## <a name="syntax"></a>Sintaxe


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProvider* \[ no\]
</dt> <dd>

Identificador para a instância do provedor. Esse identificador deve ser armazenado pelo provedor e usado em qualquer chamada subsequente. Esse identificador é válido até que a função de retorno de chamada [*PxeProviderShutdown*](pxeprovidershutdown.md) seja chamada.

</dd> <dt>

*hProviderKey* \[ no\]
</dt> <dd>

Identificador para uma chave do registro onde as informações de configuração do provedor serão armazenadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a inicialização do provedor for bem-sucedida, o retorno de chamada deverá retornar o **erro de \_ êxito**. Em caso de falha, um código de erro apropriado deve ser retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008, Windows Server 2003 com aplicativos de área de trabalho do SP2 \[ somente\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de servidor dos serviços de implantação do Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderShutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 





