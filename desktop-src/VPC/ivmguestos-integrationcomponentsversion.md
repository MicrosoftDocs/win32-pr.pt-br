---
title: Propriedade IVMGuestOS IntegrationComponentsVersion (VPCCOMInterfaces. h)
description: Recupera a versão dos componentes de integração instalados no sistema operacional convidado.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- Propriedade IntegrationComponentsVersion Virtual PC
- Propriedade IntegrationComponentsVersion Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade IntegrationComponentsVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854cb86817f461085c72a437fa962649e50ab11b65a847d0756dc8e9c7b18177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999046"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a>Propriedade IVMGuestOS:: IntegrationComponentsVersion

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a versão dos componentes de integração instalados no sistema operacional convidado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a>Valor da propriedade

A versão.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                              | Significado                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | A operação foi bem-sucedida.<br/>                                                     |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                   | O parâmetro é **NULL**.<br/>                                                        |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>           | Não foi possível encontrar a máquina virtual (VM).<br/>                                      |
| <dl> <dt>VM \_ E \_ adições \_ não \_ </dt> <dt>0xA0040504</dt> disp. </dl> | Os componentes de integração não estão instalados nesta VM ou a VM nunca foi iniciada.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>           | Ocorreu um erro inesperado.<br/>                                                 |



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

 

