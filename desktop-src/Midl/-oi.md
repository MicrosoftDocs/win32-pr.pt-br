---
title: /Oi switch
description: As opções /Oi e /Oic direcionam o compilador MIDL a usar um método de marshaling totalmente interpretado. A opção /Oicf fornece aprimoramentos de desempenho adicionais.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- /Oi switch MIDL
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38b6faee202e15b7c551297678ce301cbfdcb853b48ecd15c75dda7bb281e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385280"
---
# <a name="oi-switch"></a>/Oi switch

As **opções /Oi** e **/Oic** direcionam o compilador MIDL a usar um método de marshaling totalmente interpretado. A **opção /Oicf** fornece aprimoramentos de desempenho adicionais.

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*Oi* 
</dt> <dd>

Especifica o método totalmente interpretado para marshaling de código stub passado entre o cliente e o servidor.

> [!Note]  
> Essa opção está obsoleta. É recomendável que a **opção /Oicf** seja usada em seu lugar.

 

</dd> <dt>

*Oic* 
</dt> <dd>

Especifica o método de proxy sem código de marshaling que fornece todos os recursos **de /Oi** e também reduz ainda mais o tamanho do código stub do cliente para interfaces de objeto.

> [!Note]  
> Essa opção está obsoleta. É recomendável que a **opção /Oicf** seja usada em seu lugar.

 

</dd> <dt>

*Oif ou Oicf* 
</dt> <dd>

Especifica o método de proxy sem código de marshaling que inclui todos os recursos fornecidos por **/Oi** e **/Oic,** mas usa um novo interpretador (cadeias de caracteres de formato rápido) que fornece melhor desempenho do que **/Oi** **ou /Oic**. Essa opção inclui aprimoramentos recentes de RPC e é recomendada para cenários RPC modernos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe as restrições relacionadas a plataformas de suporte.

O compilador MIDL 3.0 fornece dois métodos para marshaling de código: totalmente interpretado ( **/Oi**, **/Oic** e **/Oicf**) e modo misto ( [**/Os**](-os.md)). A partir da versão MIDL 6.0.359, o compilador MIDL gera **/Oicf** Â [**/robust**](-robust.md) stubs por padrão. Alguns recursos de linguagem não têm suporte em alguns modos. Nesse caso, o compilador alterna automaticamente para o modo apropriado e emite um aviso.

Se o desempenho for uma preocupação, o método de modo misto ( [**/Os**](-os.md)) poderá ser a melhor abordagem. Nesse modo, o compilador opta por fazer marshal de alguns parâmetros em linha nos stubs gerados. Embora isso resulta em um tamanho maior de stub, ele oferece maior desempenho.

O método totalmente interpretado marshals de dados completamente offline. Isso reduz consideravelmente o tamanho do código stub, mas resulta em desempenho reduzido. Além disso, com o método totalmente interpretado, há um limite de 16 parâmetros para cada procedimento. Qualquer procedimento que contenha mais de 16 parâmetros será processado automaticamente no [**modo /Os.**](-os.md) Entre os modos interpretados, **/Oicf** oferece o melhor desempenho e **/Oi** oferece a melhor compatibilidade com backward.

Talvez você queira usar a opção **/Oif** se seu aplicativo usar recursos MIDL introduzidos com MIDL 3.0, como o marshal de transmissão e os atributos de \[ [**\_**](wire-marshal.md) \] marshal \[ [**\_ do**](user-marshal.md) \] usuário. Se o aplicativo usar [pipes,](/windows/desktop/Rpc/pipes) você deverá usar a **opção /Oif;** se você especificar outro modo, o compilador MIDL alterna para **/Oif**.

Para ajustar a maneira como o código stub é empacotado, o Microsoft RPC fornece um atributo de \[ [**otimização**](optimize.md) do \] ACF. Esse atributo é usado como um atributo de interface ou atributo de operação para selecionar o modo de marshaling para interfaces individuais ou para operações individuais.

### <a name="calling-conventions"></a>Convenções de chamada

Stubs gerados pelo compilador MIDL no método interpretado usando as opções **/Oi**, **/Oic** ou **/Oif** devem ser compilados como um procedimento stdcall ou cdecl durante a compilação C. Uma convenção de chamada PASCAL ou Fastcall não funcionará. Além disso, o stub do servidor deve ser compilado como stdcall.

## <a name="examples"></a>Exemplos

**midl /Oi filename.idl**

**midl /Oic filename.idl**

**midl /Oif filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**/no \_ robust**](-no-robust.md)
</dt> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/os**](-os.md)
</dt> <dt>

[**Otimizar**](optimize.md)
</dt> <dt>

[**/no \_ format \_ opt**](-no-format-opt.md)
</dt> </dl>

 

 