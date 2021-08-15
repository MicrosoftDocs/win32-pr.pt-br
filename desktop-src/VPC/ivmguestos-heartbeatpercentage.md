---
title: Propriedade HeartbeatPercentage de IVMGuestOS (VPCCOMInterfaces.h)
description: Percentual de pulsações esperadas recebidas no último minuto.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- Propriedade HeartbeatPercentage Pc Virtual
- Propriedade HeartbeatPercentage Pc Virtual , interface IVMGuestOS
- INTERFACE IVMGuestOS PC Virtual, propriedade HeartbeatPercentage
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1415b9d59e28e5658dc5b54a1a6d118e0b12a77b3208978448afb2b336f313e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753443"
---
# <a name="ivmguestosheartbeatpercentage-property"></a>Propriedade IVMGuestOS::HeartbeatPercentage

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o percentual de pulsações esperadas recebidas no último minuto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a>Valor da propriedade

O percentual de pulsações esperadas recebidas no último minuto.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                              | Significado                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | A operação foi bem-sucedida.<br/>                                                                                                            |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                   | O parâmetro é **NULL.**<br/>                                                                                                               |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>           | A configuração é desconhecida.<br/>                                                                                                            |
| <dl> <dt>VM \_ E \_ VM \_ NÃO \_ EXECUTANDO</dt> <dt>0XA0040206</dt> </dl>      | A VM (máquina virtual) deve estar em execução para essa operação.<br/>                                                                             |
| <dl> <dt>VM \_ E \_ ADIÇÕES \_ NÃO SÃO \_ 0XA0040504</dt> <dt></dt> </dl> | A VM não está totalmente inicializada, o recurso de componentes de integração não está instalado ou a versão instalada não dá suporte a esse recurso.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>           | Ocorreu um erro inesperado.<br/>                                                                                                        |



## <a name="remarks"></a>Comentários

Os componentes de integração enviarão uma pulsação periódica para Windows Virtual PC enquanto o sistema operacional convidado estiver em execução. Se o sistema operacional convidado estiver muito carregado, é possível que Windows pc virtual receba menos pulsações do que o esperado. Se o percentual de pulsação cair para zero, é possível que o sistema operacional convidado não está respondendo ou está com problema. A máquina virtual deve estar em execução (ou seja, totalmente inicializada e não desligando) e os componentes de integração devem ser instalados quando essa propriedade é invocada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS é definido como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

