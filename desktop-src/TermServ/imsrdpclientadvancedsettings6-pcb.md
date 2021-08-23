---
title: Propriedade IMsRdpClientAdvancedSettings6 PCB
description: Especifica a configuração de BLOB de preconexão (PCB) a ser usada antes de se conectar para transmissão para o servidor. | Propriedade IMsRdpClientAdvancedSettings6 PCB
ms.assetid: 3f3e6f09-2c26-44ab-9bcc-2636b71b57e2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PCB
- Propriedade PCB Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade PCB
- Propriedade PCB Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade PCB
- Propriedade PCB Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade PCB
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.PCB
- IMsRdpClientAdvancedSettings6.get_PCB
- IMsRdpClientAdvancedSettings6.put_PCB
- IMsRdpClientAdvancedSettings7.PCB
- IMsRdpClientAdvancedSettings7.get_PCB
- IMsRdpClientAdvancedSettings7.put_PCB
- IMsRdpClientAdvancedSettings8.PCB
- IMsRdpClientAdvancedSettings8.get_PCB
- IMsRdpClientAdvancedSettings8.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a68b34a04f99d830b525cadf6e35bc4816d7a52948916dc9a3d54664752dac38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001354"
---
# <a name="imsrdpclientadvancedsettings6pcb-property"></a>IMsRdpClientAdvancedSettings6::P Propriedade CB

Especifica a configuração de BLOB de preconexão (PCB) a ser usada antes de se conectar para transmissão para o servidor.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *pbstrPCB
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica a configuração de BLOB a ser usada antes da conexão.

## <a name="remarks"></a>Comentários

Essa propriedade só tem suporte nos clientes Conexão de Área de Trabalho Remota 6,1 e 7,0.

O servidor usa a configuração de BLOB para identificar o processo de destino para a conexão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





