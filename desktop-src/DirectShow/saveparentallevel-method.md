---
description: O método DVDAdm. SaveParentalLevel salva um novo nível de pai padrão no registro.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Método SaveParentalLevel (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768591"
---
# <a name="saveparentallevel-method"></a>Método SaveParentalLevel

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O método **DVDAdm. SaveParentalLevel** salva um novo nível de pai padrão no registro.

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Especifica o nível pai como valor de número inteiro de 1 a 8.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica o nome de usuário como uma cadeia de caracteres. (Ignorado no momento.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica a senha como uma cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Esse método permite que um usuário que conhece a senha atual salve uma nova configuração de nível pai no registro. Assim como acontece com todos os métodos de **MSDVDAdm**, esse método não afeta o nível atual no Player; Ele altera apenas a configuração do registro, de modo que, na próxima vez que o objeto MSWebDVD for iniciado, ele será aberto com o novo nível. Especifique-1 para desabilitar o gerenciamento de pais. Para alterar o nível de pai no Player, chame [**SelectParentalLevel**](selectparentallevel-method.md), que não altera a configuração do registro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




