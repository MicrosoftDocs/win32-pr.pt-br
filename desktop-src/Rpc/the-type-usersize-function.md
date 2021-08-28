---
title: A type_UserSize função
description: O tipo \_ função UserSize é uma função auxiliar para os atributos \ wire \_ marshal\ e \ \_ user marshal\.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f997d12e11f643eb2faf9990454a8508d15636
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886044"
---
# <a name="the-type_usersize-function"></a>O tipo \_ Função UserSize

O **&lt; tipo função &gt; \_ UserSize** é uma função auxiliar para os atributos \[ [de marshal de \_ transmissão](/windows/desktop/Midl/wire-marshal) \] e marshal \[ [ \_ de](/windows/desktop/Midl/user-marshal) \] usuário. Os stubs chamam essa função para tamanho do buffer de dados RPC para o objeto de dados do usuário antes que os dados são marshalados no lado do cliente ou do servidor. A função é definida como:

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

O &lt; tipo no nome da função significa o tipo userm, conforme especificado na definição do tipo marshal de &gt; **\[ \_ transmissão \]** ou **\[ \_ marshal \]** de usuário. Esse tipo pode ser nãotransmitível ou até mesmo , quando usado com o atributo **\[ \_ de marshal \]** do usuário, desconhecido para o compilador MIDL. O nome do tipo de transmissão (o nome do tipo transmitido pela rede) não é usado no protótipo de função. Observe, no entanto, que o tipo de transmissão define o layout dos dados conforme especificado pelo OSF DCE. Todos os dados devem ser convertidos no formato NDR (representação de dados de rede).

O *parâmetro pFlags* é um ponteiro para um **campo de sinalizador longo sem** sinal. A palavra superior do sinalizador contém sinalizadores de formato NDR, conforme definido pelo OSF DCE para representações de ponto flutuante, ordem de byte e caractere. A palavra inferior contém um sinalizador de contexto de marshaling conforme definido pelo canal COM. O layout exato dos sinalizadores dentro do campo é mostrado na tabela a seguir.



| Bits  | Sinalizador                                  | Valor                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| 31-24 | Representação de ponto flutuante         | 0 = IEEE 1 = VAX 2 = Cray 3 = IBM                                                         |
| 23-20 | Inteiro e ordem de byte de ponto flutuante | 0 = Big-endian 1 = Little-endian                                                          |
| 19-16 | Representação de caractere              | 0 = ASCII 1 = EBCDIC                                                                      |
| 15-0  | Sinalizador de contexto de marshaling               | 0 = MSHCTX \_ LOCAL 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ INPROC |



 

O sinalizador de contexto de marshaling possibilita alterar o comportamento de sua rotina, dependendo do contexto da chamada RPC. Por exemplo, se você tiver um handle (**long**) para um bloco de dados, poderá enviar o handle para uma chamada em processo, mas enviará os dados reais para uma chamada para um computador diferente. O sinalizador de contexto de marshaling e seus valores são definidos nos arquivos Wtypes.h e Wtypes.idl no SDK (Platform Software Development Kit).

> [!Note]  
> Quando o tipo de transmissão é definido corretamente, você não precisa usar os sinalizadores de formato NDR, pois o mecanismo NDR executa as conversões necessárias.

 

O *parâmetro StartingSize* é o deslocamento de buffer atual. O tamanho inicial indica o deslocamento do buffer para o objeto de usuário e pode ou não estar alinhado corretamente. Sua rotina deve levar em conta qualquer preenchimento necessário.

O *parâmetro pMyObj* é um ponteiro para um objeto de tipo de usuário.

O valor de retorno é o novo deslocamento ou a posição do buffer. A função deve retornar o tamanho cumulativo, que é o tamanho inicial mais o preenchimento possível mais o tamanho dos dados.

O **&lt; tipo função &gt; \_ UserSize** pode retornar um overestimate do tamanho necessário. O tamanho real do buffer enviado é definido pelo tamanho dos dados, não pelo tamanho da alocação do buffer.

O **&lt; tipo função &gt; \_ UserSize** não será chamado se o tamanho da transmissão puder ser calculado em tempo de compilação. Observe que, para a maioria das uniões, mesmo que não haja ponteiros, o tamanho real da representação de transmissão pode ser determinado somente em tempo de operação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Regras de marshaling para marshal \_ de usuário e \_ marshaling de transmissão](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[marshal \_ de usuário](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[wire \_ marshal](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 
