---
description: O método DVDAdm. ChangePassword salva uma nova senha de aplicativo no registro.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: Método ChangePassword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba8bfb9adcecdb88f19f3ac1b8061f93486e269
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456452"
---
# <a name="changepassword-method"></a>Método ChangePassword

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `DVDAdm.ChangePassword` método salva uma nova senha de aplicativo no registro.

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica o nome de logon do usuário atual como uma cadeia de caracteres. O objeto MSDVDAdm ignora esse parâmetro. Consulte Observações.

</dd> <dt>

<span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Gota*
</dt> <dd>

Especifica a senha antiga do usuário como uma cadeia de caracteres.

</dd> <dt>

<span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*
</dt> <dd>

Especifica a nova senha do usuário como uma cadeia de caracteres. Não pode ser uma cadeia de caracteres vazia.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Atualmente, o parâmetro *sUserName* é ignorado neste e em todos os métodos relacionados. Isso significa que quem sabe que a senha pode definir o nível de pais. Há apenas uma senha e um nível de pai para o aplicativo. Não há suporte para nomes de logon de usuário individuais ou para o gerenciamento de várias senhas. Para impor os níveis de gerenciamento dos pais, os pais devem definir a senha e, em seguida, definir o nível pai apropriado para membros mais jovens do grupo de parentes. Quando os pais desejam exibir um disco com conteúdo classificado como adulto, eles podem alterar o nível e, em seguida, alterá-lo novamente quando terminarem de ser exibidos. Desde que os filhos não saibam a senha, eles só podem ver o conteúdo no nível definido ou abaixo dele.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ConfirmPassword**](confirmpassword-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



