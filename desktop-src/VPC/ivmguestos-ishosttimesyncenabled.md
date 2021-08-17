---
title: Propriedade IVMGuestOS IsHostTimeSyncEnabled (VPCCOMInterfaces. h)
description: Indica se os componentes de integração nessa VM devem sincronizar o relógio do convidado com o relógio do host.
ms.assetid: 57e3d49c-4acf-402f-9332-58ea443b363b
keywords:
- Propriedade IsHostTimeSyncEnabled Virtual PC
- Propriedade IsHostTimeSyncEnabled Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade IsHostTimeSyncEnabled
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHostTimeSyncEnabled
- IVMGuestOS.get_IsHostTimeSyncEnabled
- IVMGuestOS.put_IsHostTimeSyncEnabled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d64482db1c4d541204fa925d10e7e1d860347183f2229449937038782e22e06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136779"
---
# <a name="ivmguestosishosttimesyncenabled-property"></a>Propriedade IVMGuestOS:: IsHostTimeSyncEnabled

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Indica se os componentes de integração nesta VM (máquina virtual) devem sincronizar o relógio do convidado com o relógio do host.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IsHostTimeSyncEnabled(
  [in]          VARIANT_BOOL shouldEnable
);

HRESULT get_IsHostTimeSyncEnabled(
  [out, retval] VARIANT_BOOL *isEnabled
);
```



## <a name="property-value"></a>Valor da propriedade

Use **Variant \_ true** se os componentes de integração nessa VM devem sincronizar o relógio do convidado com o relógio do host e a **variante \_ false** caso contrário.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>               |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro *IsEnabled* não foi especificado.<br/> |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl> | A configuração é desconhecida.<br/>               |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>           |



## <a name="remarks"></a>Comentários

Você não pode alterar essa configuração enquanto a máquina virtual estiver ativa (ou seja, em execução ou em estado salvo).

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

 

