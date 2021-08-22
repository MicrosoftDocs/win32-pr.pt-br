---
title: Propriedade IVMGuestOS TerminalServerPort
description: Porta usada por Serviços de Área de Trabalho Remota no sistema operacional convidado.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- Propriedade TerminalServerPort Virtual PC
- Propriedade TerminalServerPort Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade TerminalServerPort
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b9eea5c545613f05dbd828a9436175fab6bfc5a05ba2fe5f59588f78da913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512156"
---
# <a name="ivmguestosterminalserverport-property"></a>Propriedade IVMGuestOS:: TerminalServerPort

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Porta usada pelo Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) no sistema operacional convidado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a>Valor da propriedade

Retorna a porta usada por Serviços de Área de Trabalho Remota no sistema operacional convidado.



| Valor                                                                              | Significado                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>3389</dt> </dl>    | Valor padrão<br/>                      |
| <dl> <dt>1 65535</dt> </dl> | Intervalo válido<br/>                        |
| <dl> <dt>0</dt> </dl>       | O valor de porta válido não está disponível.<br/> |



 

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                       | Significado                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                                                 |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                                       | O Serviços de Área de Trabalho Remota ainda não foi inicializado no sistema operacional convidado.<br/> |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                            | O parâmetro *tsPort* é **nulo**.<br/>                                           |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl>               | A máquina virtual não está em execução.<br/>                                           |
| <dl> <dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt> </dl> | Os componentes de integração não estão instalados nesta máquina virtual.<br/>             |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                    | Ocorreu um erro inesperado.<br/>                                             |



## <a name="remarks"></a>Comentários

O valor dessa propriedade não é válido, a menos que a propriedade [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) seja **Variant \_ true**.

Se a propriedade [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) for **Variant \_ false** devido a um erro de conexão na porta, o valor retornado pela propriedade **TerminalServerPort** conterá o valor de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                      |
| INSERI<br/>                      | <dl> <dt>IVMGuestOS. idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

