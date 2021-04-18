---
description: O método Commit do objeto Database finaliza a forma persistente do banco de dados.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Método Database. Commit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752048"
---
# <a name="databasecommit-method"></a>Método Database. Commit

O método **Commit** do objeto [**Database**](database-object.md) finaliza a forma persistente do banco de dados. Todos os dados persistentes são gravados no banco de dado gravável e nenhuma coluna ou linha temporária é gravada. Esse método não tem efeito em um banco de dados aberto como somente leitura. Esse método pode ser chamado várias vezes para salvar o estado atual das tabelas carregadas na memória. Quando o banco de dados é finalmente fechado, as alterações feitas subsequentemente na última **confirmação** são revertidas. Esse método é normalmente chamado antes do desligamento quando todas as alterações de banco de dados tiverem sido finalizadas.

## <a name="syntax"></a>Sintaxe


```JScript
Database.Commit()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




