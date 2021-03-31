---
title: A função type_UserSize
description: A \_ função de Usersize do tipo é uma função auxiliar para os \_ atributos \ Wire Marshal e \ user \_ Marshal \.
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e5936763f9fe7b3513d66ddca7db9c35dbfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641779"
---
# <a name="the-type_usersize-function"></a>A \_ função de Usersize do tipo

A função **<type> \_ usersize** é uma função auxiliar para os \[ [atributos \_ marshaling de conexão](/windows/desktop/Midl/wire-marshal) \] e \[ [ \_ Marshal do usuário](/windows/desktop/Midl/user-marshal) \] . Os stubs chamam essa função para dimensionar o buffer de dados RPC para o objeto de dados do usuário antes que os dados sejam empacotados no lado do cliente ou do servidor. A função é definida como:

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

O <type> no nome da função significa o tipo de usuário, conforme especificado na definição de tipo de marshaling de **\[ \_ \] fio** ou de marshaling de **\[ usuário \_ \]** . Esse tipo pode ser não transmitido ou até mesmo — quando usado com o atributo **\[ \_ Marshal \] do usuário** — desconhecido para o compilador MIDL. O nome do tipo de fio (o nome do tipo transmitido pela rede) não é usado no protótipo de função. Observe, no entanto, que o tipo de conexão define o layout dos dados, conforme especificado pelo uso DCE. Todos os dados devem ser convertidos no formato de NDR (representação de dados de rede).

O parâmetro *pFlags* é um ponteiro para um campo de sinalizador **longo não assinado** . A palavra superior do sinalizador contém sinalizadores de formato NDR, conforme definido pelo uso DCE para pontos flutuantes, ordem de bytes e representações de caracteres. A palavra inferior contém um sinalizador de contexto de marshaling, conforme definido pelo canal COM. O layout exato dos sinalizadores dentro do campo é mostrado na tabela a seguir.



| Bits  | Sinalizador                                  | Valor                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| 31-24 | Representação de ponto flutuante         | 0 = IEEE 1 = VAX 2 = Cray 3 = IBM                                                         |
| 23-20 | Ordem de byte de ponto flutuante e inteiro | 0 = big-endian 1 = little-endian                                                          |
| 19-16 | Representação de caracteres              | 0 = ASCII 1 = EBCDIC                                                                      |
| 15-0  | Sinalizador de contexto de marshaling               | 0 = MSHCTX \_ local 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ InProc |



 

O sinalizador de contexto de marshaling torna possível alterar o comportamento de sua rotina, dependendo do contexto da chamada RPC. Por exemplo, se você tiver um identificador (**longo**) para um bloco de dados, poderá enviar o identificador para uma chamada em processo, mas enviaria os dados reais para uma chamada para um computador diferente. O sinalizador de contexto de marshaling e seus valores são definidos nos arquivos wtypes. h e wtypes. idl no SDK (Software Development Kit) da plataforma.

> [!Note]  
> Quando o tipo de fio é definido corretamente, você não precisa usar os sinalizadores de formato NDR, pois o mecanismo de NDR executa as conversões necessárias.

 

O *StartingSize* um parâmetro é o deslocamento do buffer atual. O tamanho inicial indica o deslocamento do buffer para o objeto de usuário e pode ou não estar alinhado corretamente. Sua rotina deve considerar qualquer preenchimento necessário.

O parâmetro *pMyObj* é um ponteiro para um objeto de tipo de usuário.

O valor de retorno é o novo deslocamento ou a posição do buffer. A função deve retornar o tamanho cumulativo, que é o tamanho inicial mais o preenchimento possível mais o tamanho dos dados.

A função **<type> \_ usersize** pode retornar um superestimar do tamanho necessário. O tamanho real do buffer enviado é definido pelo tamanho dos dados, não pelo tamanho de alocação do buffer.

A função **<type> \_ usersize** não será chamada se o tamanho da conexão puder ser calculado no momento da compilação. Observe que, para a maioria das uniões, mesmo que não haja ponteiros, o tamanho real da representação de transmissão pode ser determinado somente em tempo de execução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Marshal do usuário \_](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[\_marshaling de transmissão](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 