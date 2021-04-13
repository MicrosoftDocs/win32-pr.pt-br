---
title: Ponto de entrada VirtualChannelGetInstance
description: Chamado para que o plug-in crie uma instância da interface IWTSPlugin para todos os plug-ins implementados pela DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de ponto de entrada VirtualChannelGetInstance
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369422"
---
# <a name="virtualchannelgetinstance-entry-point"></a>Ponto de entrada VirtualChannelGetInstance

Chamado para que o plug-in crie uma instância da interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos os plug-ins implementados pela dll.

> [!Note]
>
> Essa função é implementada pelo plug-in e deve ser exportada por nome, de modo que um aplicativo possa usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a função.
>
> O protótipo para essa função não está contido em nenhum arquivo de cabeçalho público, portanto, você deve declará-lo exatamente como mostrado.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*REFIID* \[ no\]
</dt> <dd>

Especifica o tipo de interface a ser retornado. Deve ser **IID \_ IWTSPlugin**.

</dd> <dt>

*pNumObjs* \[ entrada, saída\]
</dt> <dd>

O endereço de uma variável **ULONG** que recebe o número de interfaces recuperadas.

</dd> <dt>

*ppObjArray* \[ fora\]
</dt> <dd>

O endereço de uma matriz de ponteiros que recebe os ponteiros de interface. Se esse parâmetro for **nulo**, a implementação deverá colocar o número de plug-ins implementados pela dll no parâmetro *pNumObjs* . Isso permite que o chamador aloque a matriz de tamanho apropriada para *ppObjArray*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse ponto de entrada for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



 

