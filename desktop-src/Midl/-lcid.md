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
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293329"
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

Especifica o identificador de localidade de 32 bits usado no suporte ao idioma nacional do Windows. O identificador de localidade deve ser especificado em decimal.

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

 

 




