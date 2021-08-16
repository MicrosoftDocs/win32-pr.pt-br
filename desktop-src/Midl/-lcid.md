---
title: comutador/LCID
description: A opção de compilador/LCID MIDL permite que você use caracteres internacionais em seus arquivos de entrada, nomes de arquivos e caminhos de diretório.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- MIDL do comutador/LCID
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ceff1f9a4ef2f6c95a8dac12ff689995efe4fdd3619cf48e11043967fec053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385509"
---
# <a name="lcid-switch"></a>comutador/LCID

A opção de compilador **/LCID** MIDL permite que você use caracteres internacionais em seus arquivos de entrada, nomes de arquivos e caminhos de diretório.

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*localeID* 
</dt> <dd>

especifica o identificador de localidade de 32 bits usado em Windows suporte ao idioma nacional. O identificador de localidade deve ser especificado em decimal.

</dd> </dl>

## <a name="remarks"></a>Comentários

Nos arquivos de entrada, você pode usar comentários localizados, cadeias de caracteres, HelpStrings e identificadores. Em particular, a opção **/LCID** fornece suporte completo a DBCS, para representar idiomas asiáticos, como japonês, chinês e coreano.

> [!Note]  
> A opção **/LCID** está disponível com o MIDL versão 3.01.75 e posterior.

 

## <a name="examples"></a>Exemplos

**MIDL/LCID 1041 iface. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> </dl>

 

 




