---
description: O método DVDAdm.SaveParentalLevel salva um novo nível dos pais padrão no Registro.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Método SaveParentalLevel (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e372563a6f5a1fe8e893efeb86633baa6a03a7b72c79e3f05a3ec7372bec2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315946"
---
# <a name="saveparentallevel-method"></a>Método SaveParentalLevel

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O **método DVDAdm.SaveParentalLevel** salva um novo nível dos pais padrão no Registro.

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Especifica o nível dos pais como um valor anInteger de 1 a 8.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica o nome de usuário como uma Cadeia de Caracteres. (Atualmente ignorado.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica a senha como uma Cadeia de Caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Esse método permite que um usuário que conhece a senha atual salve uma nova configuração de nível dos pais no Registro. Assim como acontece com todos os métodos **de MSDVDAdm**, esse método não afeta o nível atual no player; ele altera apenas a configuração do Registro, de modo que na próxima vez que o objeto MSWebDVD for iniciado, ele será aberto com o novo nível. Especifique -1 para desabilitar o gerenciamento dos pais. Para alterar o nível dos pais no player, [**chame SelectParentalLevel**](selectparentallevel-method.md), que não altera a configuração do Registro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




