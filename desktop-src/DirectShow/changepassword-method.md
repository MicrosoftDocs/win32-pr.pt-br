---
description: O método DVDAdm.ChangePassword salva uma nova senha de aplicativo no Registro.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: Método ChangePassword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f5d15eef943afa019f1b1bba4e3b1412978bc5dd8f52f411c504e880428848a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999326"
---
# <a name="changepassword-method"></a>Método ChangePassword

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `DVDAdm.ChangePassword` método salva uma nova senha de aplicativo no Registro.

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica o nome de logon do usuário atual como uma Cadeia de Caracteres. O objeto MSDVDAdm ignora esse parâmetro. Consulte Observações.

</dd> <dt>

<span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Vendido*
</dt> <dd>

Especifica a senha antiga do usuário como uma Cadeia de Caracteres.

</dd> <dt>

<span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*
</dt> <dd>

Especifica a nova senha do usuário como uma Cadeia de Caracteres. Não pode ser uma cadeia de caracteres vazia.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Atualmente, o *parâmetro sUserName* é ignorado neste e em todos os métodos relacionados. Isso significa que quem sabe a senha pode definir o nível dos pais. Há apenas uma senha e um nível dos pais para o aplicativo. Não há suporte para nomes de logon de usuário individuais ou gerenciamento de várias senhas. Para impor níveis de gerenciamento dos pais, os pais devem definir a senha e, em seguida, definir o nível dos pais apropriado para membros mais novos do grupo de crianças. Quando os pais quiserem exibir um disco com conteúdo com classificação para adulto, eles poderão alterar o nível e, em seguida, alterá-lo novamente quando terminarem de exibir. Desde que os filhos não saibam a senha, eles só podem assistir ao conteúdo no nível definido ou abaixo deles.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Confirmpassword**](confirmpassword-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



