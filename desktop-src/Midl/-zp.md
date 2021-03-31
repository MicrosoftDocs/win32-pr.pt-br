---
title: Comutador/ZP
description: O comutador/ZP é o mesmo que a opção/Pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- MIDL do comutador/ZP
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638455"
---
# <a name="zp-switch"></a>Comutador/ZP

O comutador **/ZP** é o mesmo que a opção [**/Pack**](-pack.md) .

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*nível de embalagem \_* 
</dt> <dd>

Especifica o nível de empacotamento das estruturas no sistema de destino. O valor de nível de embalagem pode ser definido como 1, 2, 4 ou 8.

</dd> </dl>

## <a name="remarks"></a>Comentários

A opção **/ZP** designa o nível de empacotamento das estruturas no sistema de destino. O valor de nível de embalagem corresponde ao valor de opção **/ZP** usado pelo compilador C/C++ da Microsoft. Para obter mais informações, consulte a documentação de programação do Microsoft C/C++.

Especifique o mesmo nível de embalagem ao invocar o compilador MIDL e o compilador C.

O nível de empacotamento padrão usado quando nem a opção **/ZP** nem [**/Pack**](-pack.md) é especificada é 8 em todos os ambientes de compilação.

> [!Note]  
> Não use **/Zp1** ou **/ZP2** em plataformas MIPS ou Alpha e não use **/Zp4** ou **/Zp8** em plataformas de 16 bits. Dependendo do tipo de dados e do local da memória atribuído pelo compilador C em tempo de execução, isso pode resultar em uma exceção de desalinhamento de dados em plataformas MIPS e Alpha. Em plataformas MS-DOS, o compilador C não garantirá o alinhamento em 4 ou 8 e, portanto, o aplicativo poderá ser encerrado.

 

## <a name="examples"></a>Exemplos

**MIDL/Zp4 filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Pack**](-pack.md)
</dt> </dl>

 

 




