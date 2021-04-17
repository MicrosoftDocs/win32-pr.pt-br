---
description: O método DVDAdm. ConfirmPassword testa se a senha especificada corresponde à senha salva anteriormente.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: Método ConfirmPassword (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755587"
---
# <a name="confirmpassword-method"></a>Método ConfirmPassword

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `DVDAdm.ConfirmPassword` método testa se a senha especificada corresponde à senha salva anteriormente.

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica o nome do usuário como uma cadeia de caracteres.

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica a nova senha como uma cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará true se a senha especificada corresponder à senha existente; caso contrário, retorna false.

## <a name="remarks"></a>Comentários

Atualmente, o parâmetro *sUserName* é ignorado neste e em todos os métodos relacionados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ChangePassword**](changepassword-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




