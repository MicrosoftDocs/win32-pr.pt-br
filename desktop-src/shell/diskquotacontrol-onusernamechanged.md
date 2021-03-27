---
description: Ocorre quando as informações de nome de um objeto DIDiskQuotaUser são resolvidas.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Função onusernamechanged (Dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296936"
---
# <a name="onusernamechanged-function"></a>Função onusernamechanged

Ocorre quando as informações de nome de um objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) são resolvidas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*oUser* 
</dt> <dd>

O **objeto** que é avaliado para o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) associado ao usuário cujo nome foi resolvido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Quando um cliente [**enumera os usuários**](didiskquotauser-object.md)ou chama o método [**adduser**](diskquotacontrol-adduser.md) ou [**FindUser**](diskquotacontrol-finduser.md) , o nome de usuário deve ser resolvido para o Sid (ID de segurança) associado. Como esse procedimento pode ser demorado, um cliente pode ter a resolução de nomes feita de forma assíncrona em um thread em segundo plano. Quando o nome de um usuário é resolvido, o objeto [**DiskQuotaControl**](diskquotacontrol-object.md) notifica seu cliente acionando o evento **onnomedeusuáriochanged** . Um objeto **DIDiskQuotaUser** associado ao usuário é passado como um parâmetro. Esse objeto permite que o cliente modifique as configurações de cota do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




