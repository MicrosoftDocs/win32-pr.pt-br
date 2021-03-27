---
description: Define ou Obtém um valor que controla como o SID (identificador de segurança do usuário) é resolvido para nomes de usuário.
title: Propriedade DiskQuotaControl. UserNameResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: fbe079680191937f022bd45a491fad054e1a9033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967389"
---
# <a name="diskquotacontrolusernameresolution-property"></a>Propriedade DiskQuotaControl. UserNameResolution

Define ou Obtém um valor que controla como o SID (identificador de segurança do usuário) é resolvido para nomes de usuário.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade pode ser definida como um dos valores a seguir.



| Tipo de resolução | Valor | Descrição                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| dqResolveNone   | 0     | Não resolva as informações de nome de usuário.                                                                                                                    |
| dqResolveSync   | 1     | Aguarde enquanto resolve informações de nome.                                                                                                                   |
| dqResolveAsync  | 2     | Não aguarde enquanto as informações de nome são resolvidas. O evento [**Onusernamechanged**](diskquotacontrol-onusernamechanged.md) é acionado quando o nome é resolvido. |



 

## <a name="remarks"></a>Comentários

Essa propriedade afeta a enumeração de objetos [**DIDiskQuotaUser**](didiskquotauser-object.md) e os métodos [**adduser**](diskquotacontrol-adduser.md) e [**FindUser**](diskquotacontrol-finduser.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




