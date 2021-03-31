---
title: Comutador/Oi
description: As opções/Oi e/OIC orientam o compilador MIDL a usar um método de marshaling totalmente interpretado. A opção/Oicf fornece aprimoramentos de desempenho adicionais.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- MIDL do comutador/Oi
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104161922"
---
# <a name="oi-switch"></a>Comutador/Oi

As opções **/Oi** e **/OIC** orientam o compilador MIDL a usar um método de marshaling totalmente interpretado. A opção **/Oicf** fornece aprimoramentos de desempenho adicionais.

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*Oi* 
</dt> <dd>

Especifica o método totalmente interpretado para o empacotamento do código stub passado entre o cliente e o servidor.

> [!Note]  
> Essa opção é obsoleta. É recomendável que a opção **/Oicf** seja usada em seu lugar.

 

</dd> <dt>

*Oic* 
</dt> <dd>

Especifica o método de proxy sem código de marshaling que fornece todos os recursos do **/Oi** e também reduz ainda mais o tamanho do código stub do cliente para interfaces de objeto.

> [!Note]  
> Essa opção é obsoleta. É recomendável que a opção **/Oicf** seja usada em seu lugar.

 

</dd> <dt>

*OIF ou Oicf* 
</dt> <dd>

Especifica o método de proxy sem código de marshaling que inclui todos os recursos fornecidos por **/Oi** e **/OIC** , mas usa um novo interpretador (cadeias de caracteres de formato rápido) que fornece melhor desempenho do que o **/Oi** ou o **/OIC**. Essa opção inclui aprimoramentos de RPC recentes e é recomendada para cenários de RPC modernos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe as restrições relacionadas às plataformas de suporte.

O compilador MIDL 3,0 fornece dois métodos para empacotamento de código: totalmente interpretado ( **/Oi**, **/OIC** e **/Oicf**) e [**/os**](-os.md)(modo misto). Começando com o MIDL versão 6.0.359, o compilador MIDL gera stubs **/Oicf** Â  [**/robust**](-robust.md) por padrão. Alguns recursos de linguagem não têm suporte em alguns modos. Nesse caso, o compilador alterna automaticamente para o modo apropriado e emite um aviso.

Se o desempenho for uma preocupação, o método de modo misto ( [**/os**](-os.md)) pode ser a melhor abordagem. Nesse modo, o compilador escolhe realizar marshaling de alguns parâmetros embutidos nos stubs gerados. Embora isso resulte em um tamanho maior de stub, ele oferece maior desempenho.

O método totalmente interpretado realiza marshaling de dados completamente offline. Isso reduz consideravelmente o tamanho do código stub, mas resulta em desempenho reduzido. Além disso, com o método totalmente interpretado, há um limite de 16 parâmetros para cada procedimento. Qualquer procedimento que contenha mais de 16 parâmetros será automaticamente processado no modo [**/os**](-os.md) . Entre os modos interpretados, o **/Oicf** oferece o melhor desempenho e o **/Oi** oferece a melhor compatibilidade com versões anteriores.

Talvez você queira usar a opção **/OIF** se seu aplicativo usar recursos de MIDL que foram introduzidos com MIDL 3,0, como os \[ atributos de [**\_ marshaling de conexão**](wire-marshal.md) \] e de \[ [**\_ marshaling do usuário**](user-marshal.md) \] . Se seu aplicativo usa [pipes](/windows/desktop/Rpc/pipes) , você deve usar a opção **/OIF** ; Se você especificar outro modo, o compilador MIDL será alternado para **/OIF**.

Para ajustar a maneira como seu código de stub é empacotado, o Microsoft RPC fornece um atributo de ACF \[ [**Optimize**](optimize.md) \] . Esse atributo é usado como um atributo de interface ou atributo de operação para selecionar o modo de marshaling para interfaces individuais ou para operações individuais.

### <a name="calling-conventions"></a>Convenções de chamada

Os stubs gerados pelo compilador MIDL no método interpretado usando as opções **/Oi**, **/OIC** ou **/OIF** devem ser compilados como um procedimento stdcall ou cdecl durante a compilação de C. Uma Convenção de chamada PASCAL ou fastcall não funcionará. Além disso, o stub do servidor deve ser compilado como stdcall.

## <a name="examples"></a>Exemplos

**MIDL/Oi filename. idl**

**MIDL/OIC filename. idl**

**MIDL/OIF filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**// \_ avançado**](-no-robust.md)
</dt> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Os**](-os.md)
</dt> <dt>

[**formato**](optimize.md)
</dt> <dt>

[**\_opção de formato de/// \_**](-no-format-opt.md)
</dt> </dl>

 

 