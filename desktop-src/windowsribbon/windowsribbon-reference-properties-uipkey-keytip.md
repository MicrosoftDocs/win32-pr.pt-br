---
title: UI_PKEY_Keytip
description: Identifica a \_ Propriedade PKEY KeyTip da interface do usuário \_ .
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916339"
---
# <a name="ui_pkey_keytip"></a>\_KeyTip PKEY \_ UI

Identifica a \_ Propriedade PKEY KeyTip da interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ KeyTip é usada por um aplicativo para consultar o acelerador de teclado de um controle da faixa de faixas.

Esse valor de propriedade é uma cadeia de caracteres, composta de qualquer sequência de caracteres, incluindo o espaço em branco.

O valor da interface do usuário \_ PKEY \_ KeyTip atua como o acelerador de teclado para um comando, a menos que esse comando seja exposto por meio de um item de menu. Nesse caso, a estrutura ignora o valor da interface do usuário \_ PKEY \_ KeyTip e, em vez disso, usa um caractere precedido por um e comercial como especificado por [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou pelo [ \_ \_ rótulo de PKEY da interface do usuário](windowsribbon-reference-properties-uipkey-label.md). Se nenhum e comercial for especificado pelo **comando Command. LabelTitle** ou UI \_ PKEY \_ , nenhum KeyTip ou acelerador de teclado será exposto.

O comprimento máximo da interface do usuário \_ PKEY \_ KeyTip é não associado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do recurso](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Comando. KeyTip**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




