---
title: Método IVMGuestOS IsUserLoggedOn (VPCCOMInterfaces. h)
description: Determina se a sessão solicitada está presente.
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- IsUserLoggedOn do método virtual PC
- Método IsUserLoggedOn Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, método IsUserLoggedOn
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810652"
---
# <a name="ivmguestosisuserloggedon-method"></a>Método IVMGuestOS:: IsUserLoggedOn

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se a sessão solicitada está presente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inRailSession* \[ no\]
</dt> <dd>

Defina como 0 para uma sessão de trilho ou 1 para uma sessão de RDP.

</dd> <dt>

*outSessionPresent* \[ out, retval\]
</dt> <dd>

Defina como **Variant \_ true** se a sessão estiver presente e **Variant \_ false** caso contrário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                       | Descrição                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                             | A operação foi bem-sucedida.<br/>                                   |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                               | O parâmetro é **NULL**.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                            | O parâmetro *outSessionPresent* não é válido ou é **nulo**.<br/>  |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                       | Ocorreu um erro inesperado.<br/>                               |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (erro \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt> </dl> | Não há memória suficiente disponível para concluir esta solicitação.<br/>  |
| <dl> <dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt> </dl>                        | A operação não foi concluída oportunamente.<br/>              |
| <dl> <dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt> </dl>                  | A máquina virtual (VM) deve estar em execução para esta operação.<br/>    |
| <dl> <dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt> </dl>    | O recurso componentes de integração não está instalado nesta VM.<br/> |
| <dl> <dt>**VM \_ E \_ VM em \_ pausa**</dt> <dt>0xA00400507</dt> </dl>                       | A VM está pausada.<br/>                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

