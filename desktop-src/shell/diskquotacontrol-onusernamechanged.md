---
description: Ocorre quando as informações de nome de um objeto DIDiskQuotaUser foram resolvidas.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Função OnUserNameChanged (Dskquota.h)
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
ms.openlocfilehash: 02e4227e06d9c9303a5fe9b799afff6e452843bbb7c0dac096b39f925e568d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459889"
---
# <a name="onusernamechanged-function"></a>Função OnUserNameChanged

Ocorre quando as informações de nome de [**um objeto DIDiskQuotaUser**](didiskquotauser-object.md) foram resolvidas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*oUser* 
</dt> <dd>

O **Objeto** que é avaliada para o [**objeto DIDiskQuotaUser**](didiskquotauser-object.md) associado ao usuário cujo nome foi resolvido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Quando um cliente [**enumera usuários**](didiskquotauser-object.md)ou chama o [**método AddUser**](diskquotacontrol-adduser.md) ou [**FindUser,**](diskquotacontrol-finduser.md) o nome de usuário deve ser resolvido para a SID (ID de segurança) associada. Como esse procedimento pode ser demorado, um cliente pode ter a resolução de nomes feita de forma assíncrona em um thread em segundo plano. Quando o nome de um usuário é resolvido, o objeto [**DiskQuotaControl**](diskquotacontrol-object.md) notifica seu cliente disparando o **evento OnUserNameChanged.** Um **objeto DIDiskQuotaUser** associado ao usuário é passado como um parâmetro. Esse objeto permite que o cliente modifique as configurações de cota do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Dskquota.h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




