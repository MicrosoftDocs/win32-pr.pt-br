---
title: Propriedade IVMGuestOS HeartbeatPercentage (VPCCOMInterfaces. h)
description: Porcentagem de pulsações esperadas recebidas no último minuto.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- Propriedade HeartbeatPercentage Virtual PC
- Propriedade HeartbeatPercentage Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade HeartbeatPercentage
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
# <a name="ivmguestosheartbeatpercentage-property"></a>Propriedade IVMGuestOS:: HeartbeatPercentage

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a porcentagem de pulsações esperadas recebidas no último minuto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a>Valor da propriedade

A porcentagem de pulsações esperadas recebidas no último minuto.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                              | Significado                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | A operação foi bem-sucedida.<br/>                                                                                                            |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                   | O parâmetro é **NULL**.<br/>                                                                                                               |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>           | A configuração é desconhecida.<br/>                                                                                                            |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl>      | A máquina virtual (VM) deve estar em execução para esta operação.<br/>                                                                             |
| <dl> <dt>VM \_ E \_ adições \_ não \_ </dt> <dt>0xA0040504</dt> disp. </dl> | A VM não está totalmente inicializada, o recurso componentes de integração não está instalado ou a versão instalada não oferece suporte a esse recurso.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>           | Ocorreu um erro inesperado.<br/>                                                                                                        |



## <a name="remarks"></a>Comentários

os componentes de integração enviarão uma pulsação periódica para Windows Virtual PC enquanto o sistema operacional convidado estiver em execução. se o sistema operacional convidado estiver muito carregado, será possível que Windows Virtual PC receba menos pulsações do que o esperado. Se a porcentagem de pulsação cair para zero, é possível que o sistema operacional convidado não esteja respondendo ou tenha falhado. A máquina virtual deve estar em execução (ou seja, totalmente inicializada e não desligada) e os componentes de integração devem ser instalados quando essa propriedade é chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

