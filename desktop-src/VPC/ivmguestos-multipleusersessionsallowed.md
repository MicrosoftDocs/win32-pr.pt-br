---
title: Propriedade IVMGuestOS MultipleUserSessionsAllowed
description: Determina se várias sessões de usuário simultâneas são permitidas no sistema operacional convidado.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- Propriedade MultipleUserSessionsAllowed Virtual PC
- Propriedade MultipleUserSessionsAllowed Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade MultipleUserSessionsAllowed
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085652"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a>Propriedade IVMGuestOS:: MultipleUserSessionsAllowed

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se várias sessões de usuário simultâneas são permitidas no sistema operacional convidado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a>Valor da propriedade

**Variante \_ TRUE** se várias sessões de usuário simultâneas forem permitidas no sistema operacional convidado; caso contrário, **Variant \_ false** .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                       | Significado                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                                                                                       |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                                       | Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) ainda não foi inicializado no sistema operacional convidado.<br/> |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                            | O parâmetro *sessionStatus* é **nulo**.<br/>                                                                          |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl>               | A máquina virtual não está em execução.<br/>                                                                                 |
| <dl> <dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt> </dl> | Os componentes de integração não estão instalados nesta máquina virtual.<br/>                                                   |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                    | Ocorreu um erro inesperado.<br/>                                                                                   |



## <a name="remarks"></a>Comentários

O valor dessa propriedade não é válido, a menos que a propriedade [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) seja **Variant \_ true**.

Para sistemas operacionais cliente do Windows, **MultipleUserSessionsAllowed** será **Variant \_ true** se houver suporte para troca rápida de usuário. Para sistemas operacionais Windows Server, **MultipleUserSessionsAllowed** será **VARIANT \_ true** se serviços de área de trabalho remota (anteriormente chamado de serviços de terminal) estiver instalado e habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                      |
| INSERI<br/>                      | <dl> <dt>IVMGuestOS. idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

