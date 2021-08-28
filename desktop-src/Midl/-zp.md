---
title: Opção /Zp
description: A opção /Zp é a mesma que a opção /pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- /Zp switch MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1795068aae1a5a8c3e793b828d5a80dbab369e16f9c5383af367b66d0febc738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067436"
---
# <a name="zp-switch"></a>Opção /Zp

A **opção /Zp** é a mesma que a [**opção /pack.**](-pack.md)

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*nível de \_ empacotamento* 
</dt> <dd>

Especifica o nível de empacotamento de estruturas no sistema de destino. O valor de nível de empacotamento pode ser definido como 1, 2, 4 ou 8.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **opção /Zp** designa o nível de empacotamento de estruturas no sistema de destino. O valor de nível de empacotamento corresponde ao valor da opção **/Zp** usado pelo compilador do Microsoft C/C++. Para obter mais informações, consulte a documentação de programação do Microsoft C/C++.

Especifique o mesmo nível de empacotamento ao invocar o compilador MIDL e o compilador C.

O nível de empacotamento padrão usado quando nem a **opção /Zp** nem [**/pack**](-pack.md) é especificada é 8 em todos os ambientes de build.

> [!Note]  
> Não use **/Zp1** ou **/Zp2** em plataformas MIPS ou Alfa e não use **/Zp4** ou **/Zp8** em plataformas de 16 bits. Dependendo do tipo de dados e do local de memória atribuídos pelo compilador C em tempo de executar, isso pode resultar em uma exceção de desalinhamento de dados em plataformas MIPS e Alfa. Em plataformas MS-DOS, o compilador C não garantirá o alinhamento em 4 ou 8 e, portanto, o aplicativo poderá ser encerrado.

 

## <a name="examples"></a>Exemplos

**midl /Zp4 filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/pack**](-pack.md)
</dt> </dl>

 

 




