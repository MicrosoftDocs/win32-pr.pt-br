---
description: O conceito de um endereço é essencial para a maioria das operações de comunicação.
ms.assetid: 32fbd06b-f6f2-4024-b8d5-3d6eef16bca2
title: Endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6ad8f03b725a58d564c63f4c5c0d0165eed99a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766241"
---
# <a name="address"></a>Endereço

O conceito de um endereço é essencial para a maioria das operações de comunicação. Um endereço representa um local em uma rede. A atribuição local de um endereço a uma linha ou canal normalmente ocorre durante a instalação do provedor de serviços, mas pode ser modificada posteriormente. Detalhes sobre os procedimentos envolvidos podem ser encontrados no kit de recursos do sistema operacional para provedores de serviços fornecidos pela Microsoft e na documentação do provedor de serviços para produtos que não são da Microsoft.

Um único endereço pode ser compartilhado por mais de um dispositivo de linha. Fornecedores de comutadores diferentes têm nomes diferentes para esse conceito, como ponte de endereço, número de diretório de aparência múltipla (MADN) ou aparência de ponte. Uma chamada de entrada em um endereço compartilhado é oferecida em todas as linhas associadas ao endereço. Consulte [ \_ constantes LINEADDRESSSHARING](./lineaddresssharing--constants.md) para obter uma descrição das configurações que a TAPI reconhece.

O endereço em si é uma cadeia de caracteres que identifica um local em uma rede. No caso de uma rede telefônica, o endereço é um número de telefone completo com códigos nacionais ou internacionais. Se a rede for baseada em IP, o endereço poderá ser um endereço IP. Consulte [ \_ constantes LINEADDRESSTYPE](lineaddresstype--constants.md) para tipos de endereço definidos pela TAPI. Um provedor de serviços pode definir tipos de endereço adicionais.

## <a name="address-related-capabilities-and-messages"></a>Address-Related recursos e mensagens

Endereços diferentes têm recursos, funcionalidades e Estados diferentes. Os provedores de serviços são a fonte dessas informações. Os mecanismos de recurso de consulta de dispositivo e status e relatório de eventos da TAPI fornecem a um aplicativo as informações para gerenciar endereços.

Os aplicativos adquirem essas informações processando eventos da TAPI ou usando operações de consulta. Isso permite que um aplicativo leve em consideração fatores como, por exemplo, se um determinado endereço dá suporte a um recurso específico, como o [Parque](park-ovr.md).

**TAPI 2. x:** Os aplicativos chamam a função [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) para determinar os recursos de telefonia de cada endereço e, em seguida, recebe essas informações em uma estrutura de dados [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) . De forma semelhante, um aplicativo pode chamar [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) para um dispositivo de linha para determinar o número de endereços atribuídos à linha, bem como outras informações.

**TAPI 3. x:** Os aplicativos usam as [interfaces de objeto de endereço](address-object-interfaces.md) para adquirir informações sobre recursos e eventos de endereço.

## <a name="storing-phone-numbers-in-electronic-address-books"></a>Armazenando números de telefone em catálogos de endereços eletrônicos

Muitos usuários optam por discar pessoas, máquinas de fax, BBS e outras entidades selecionando seus nomes em um catálogo de endereços. O número real discado depende da localização geográfica do usuário e da maneira como o dispositivo de linha a ser usado está conectado. Por exemplo, um computador desktop pode ter acesso a duas linhas, uma conectada a um PBX, a outra para o escritório central da companhia telefônica. Ao fazer uma chamada para a mesma entidade, podem ser usados números diferentes. (Para discar por meio do PBX, por exemplo, o computador pode precisar discar um prefixo "9" para obter uma linha externa ou um prefixo diferente pode ser necessário para uma chamada feita por meio do escritório central.) Ou, um usuário pode fazer chamadas de um computador portátil e usar um único catálogo de endereços estáticos mesmo ao chamar de locais diferentes ou ambientes de telefonia. Os recursos de conversão de endereço da TAPI permitem que o usuário informe o computador do local atual e o dispositivo de linha desejado para a chamada. Em seguida, a TAPI manipula quaisquer diferenças de discagem, não exigindo nenhuma alteração no catálogo de endereços do usuário. Um aplicativo usa a [conversão de endereços](initiate-a-session-ovr.md) para converter um endereço do formato de [endereço canônico](#canonical-addresses) no formato de [endereço de discagem](#dialable-addresses) .

Um tópico relacionado é o tratamento de monitoramento de andamento de chamada internacional, que é o processo de escuta de tons audíveis, como Tom de discagem, tons de informações especiais, sinais ocupados e tons de toque para determinar o *estado* de uma chamada (seu progresso pela rede). Como as cadências e frequências dos tons de avanço de chamada variam de país ou região para país ou região, o provedor de serviços deve saber o que o andamento da chamada seguir ao fazer uma chamada internacional de saída. Portanto, os aplicativos especificam o código de país ou região de destino ao colocar chamadas de saída.

## <a name="canonical-addresses"></a>Endereços canônicos

O formato de endereço canônico deve ser um número de diretório universalmente constante. Por esse motivo, os números nos catálogos de endereços são melhor armazenados usando o formato canônico.

Os detalhes a seguir referem-se ao que é considerado canônico para um endereço de telefone.

Um endereço de telefone canônico é uma cadeia de caracteres de texto com a seguinte estrutura:

\+*CountryCode* Space \[ **(**_AreaCode_*_)_* espaço \] *SubscriberNumber* \| nome do *Subendereço*  ^   CRLF...

Os componentes dessa estrutura são descritos na tabela a seguir.



Componente

Significado

\+

Equivalente a hex 2B. Indica que o número a seguir usa o formato canônico.

*CountryCode*

Uma cadeia de caracteres de tamanho variavelmente contendo um ou mais dos dígitos "0" a "9" (de 30 a 39, inclusive). O *CountryCode* é delimitado pelo espaço a seguir. Ele identifica o país ou região em que o endereço está localizado.

Space

Exatamente um caractere de espaço (hexadecimal 20). Ele é usado para delimitar o final da parte *CountryCode* de um endereço.

*AreaCode*

Uma cadeia de caracteres de tamanho variavelmente contendo zero ou mais dos dígitos "0" a "9" (de 30 a 39, inclusive). *AreaCode* é a parte do código de área do endereço e é opcional. Se o código de área estiver presente, ele deverá ser precedido por exatamente um caractere de parêntese esquerdo (28) e será seguido por exatamente um caractere de parêntese direito (29) e um caractere de espaço (20).

*SubscriberNumber*

Uma cadeia de caracteres de tamanho variavelmente contendo um ou mais dos dígitos "0" a "9" (de 30 a 39, inclusive). Ele também pode incluir outros caracteres de formatação, incluindo qualquer um dos caracteres de controle de discagem descritos no formato de endereço discável:

 

Caractere

Codificação hexadecimal

 

! \#<br/> $<br/> \*<br/> ,<br/> ?<br/> @<br/> ABCD<br/> P<br/> T<br/> W<br/> abcd<br/> p<br/> t<br/> w<br/>

21 23<br/> 24<br/> 2A<br/> 2C<br/> 3F<br/> 40<br/> 41-44<br/> 50<br/> 54<br/> 77<br/> 61-64<br/> 70<br/> 74<br/> 79<br/>

 

O número do assinante não deve conter o caractere de parêntese esquerdo ou parêntese direito (que são usados apenas para delimitar o código de área), nem deve conter os \| caracteres "", "^" ou CRLF (que são usados para iniciar os campos a seguir). Normalmente, os caracteres não-dígitos no número do assinante incluem apenas espaços, pontos (".") e traços ("-"). Quaisquer caracteres não-numéricos permitidos que apareçam no número do Assinante são omitidos de *discstring* retornados pela função [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) , mas são retidos na *disreproduçãostring*.

\|

Hex (7C). Se esse caractere opcional estiver presente, as informações que o seguem para o próximo + \| ^ CRLF ou o final da cadeia de caracteres de endereço canônico serão tratadas como informações de Subendereço, como para um subendereço ISDN.

*Subendereço*

Uma cadeia de caracteres de tamanho variavelmente contendo um subendereço. A cadeia de caracteres é delimitada por + \| ^ CRLF ou o final da cadeia de caracteres de endereço. Durante a discagem, as informações de Subendereço são passadas para a parte remota. Ele pode ser algo como um subendereço ISDN ou um endereço de email.

^

Hex (5E). Se esse caractere opcional estiver presente, as informações que o seguem até o próximo CRLF ou o final da cadeia de caracteres de endereço canônico serão tratadas como um nome ISDN.

*Nome*

Uma cadeia de caracteres de tamanho variavelmente tratada como informações de nome. O nome é delimitado por CRLF ou pelo fim da cadeia de caracteres de endereço canônico e pode conter outros delimitadores. Durante a discagem, as informações de nome são passadas para a parte remota.

CRLF

Hex (0D) seguido de hex (0A) e é opcional. Se presente, indica que outro número canônico está seguindo este. Ele é usado para separar vários endereços canônicos como parte de uma única cadeia de caracteres de endereço (multiplexação inversa). Por exemplo, a representação canônica do número de telefone do menu de controle principal na Microsoft Corporation seria:<br/> + 1 (425) 882-8080<br/>



 

## <a name="dialable-addresses"></a>Endereços de discagem

O formato de endereço de discagem é o formulário no qual um endereço é passado para um provedor de serviços que lida com números de telefone. Os detalhes a seguir se referem a endereços de discagem em uma rede de telefone.

O formato de número de discagem permite que vários endereços de destino sejam fornecidos ao mesmo tempo. Essa capacidade pode ser útil se o provedor de serviços oferece alguma forma de multiplexação inversa, configurando chamadas para cada um dos destinos especificados e gerenciando o fluxo de informações como um único fluxo de mídia de alta largura de banda. O aplicativo percebe esse grupo de chamadas como uma única chamada porque recebe apenas um único identificador de chamada que representa a agregação das chamadas telefônicas individuais.

Também é possível dar suporte à multiplexação inversa no nível do aplicativo. Para fazer isso, o aplicativo configuraria uma série de chamadas individuais e sincronizaria seus fluxos de mídia.

O *Subendereço* é um recurso fornecido em linhas ISDN que permite mais informações do que apenas um único número de telefone a ser usado durante a discagem. Essas informações adicionais podem especificar uma extensão telefônica individual para tocar ou, em um ambiente computacional, em um determinado aplicativo a ser alertado. Outros parâmetros podem descrever os aspectos necessários de uma conexão solicitada, como taxa e tempo.

Se o Subendereço for suportado por um provedor de serviços, o aplicativo incluirá isso no endereço passado para qualquer operação que exija um.

Um endereço de telefone de discagem contém informações de endereçamento de parte e faz parte da navegação por natureza. Qualquer cadeia de caracteres de entrada que não comece com um caractere "+" provavelmente não estará no formato canônico e, portanto, estará no formato de endereço de discagem e será retornada para o aplicativo não modificado. Um endereço de discagem é uma cadeia de caracteres de texto com a seguinte estrutura:

*DialableNumber* \| *Subendereço*  ^  *Nome* do CRLF...

Os componentes dessa estrutura são fornecidos na tabela a seguir.



| Componente        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DialableNumber* | Dígitos e modificadores 0-9 A-D \* \# ,! W w P p T t @ $? ; delimitado por \| ^ CRLF ou o fim da cadeia de caracteres de endereço de discagem. O sinal de adição (+) é um caractere válido em cadeias de caracteres de discagem. Ele indica que o número de telefone é um número internacional totalmente qualificado. Dentro do *DialableNumber*, observe as seguintes definições:<br/> 0-9 a-D \*\#<br/> Caracteres correspondentes aos dígitos DTMF e/ou Pulse.<br/> |
| !                | Hex (21). Indica que um hookflash (um meio secundário, seguido por um meio segundo offhook antes de continuar) deve ser inserido na cadeia de caracteres de discagem.                                                                                                                                                                                                                                                                                   |
| P p              | Hex (50) ou hex (70). Indica que a discagem de pulso deve ser usada para os dígitos após ele.                                                                                                                                                                                                                                                                                                                                                |
| T t              | Hex (54) ou hex (74). Indica que a discagem de Tom (DTMF) deve ser usada para os dígitos após ele.                                                                                                                                                                                                                                                                                                                                          |
| ,                | Hex (27). Indica que a discagem deve ser pausada. A duração de uma pausa é específica do dispositivo e pode ser recuperada dos recursos do dispositivo da linha. Várias vírgulas podem ser usadas para fornecer mais pausas.                                                                                                                                                                                                                                 |
| W w              | Hex (57) ou hex (77). Uma letra maiúscula ou minúscula W indica que a discagem deve continuar somente após a detecção de um tom de discagem.                                                                                                                                                                                                                                                                                                            |
| @                | Hex (40). Indica que a discagem é "aguardar resposta silenciosa" antes de discar o restante do endereço de discagem. Isso significa aguardar pelo menos um tom de toque seguido por vários segundos de silêncio.                                                                                                                                                                                                                               |
| $                | Hex (24). Indica que a discagem das informações de cobrança é aguardar por um "sinal de cobrança" (como um tom de prompt de cartão de crédito).                                                                                                                                                                                                                                                                                                              |
| ?                | Hex (3F). Indica que o usuário deve ser solicitado antes de continuar com a discagem. O provedor não faz a solicitação de fato, mas a presença de "?" força o provedor a rejeitar a cadeia de caracteres como inválida, alertando o aplicativo para a necessidade de dividi-lo em partes e solicitar o usuário entre eles.                                                                                                                           |
| ;                | Hex (3B). Se colocado no final de uma cadeia de caracteres de endereço de discagem parcialmente especificada, isso indica que as informações de número de discagem estão incompletas e mais informações de endereço serão fornecidas posteriormente. O componente ";" só é permitido na parte *DialableNumber* de um endereço.                                                                                                                                                       |
| \|               | Hex (7C) e é opcional. Se presente, as informações que o seguem para o próximo + \| ^ CRLF ou o final da cadeia de caracteres de endereço de discagem serão tratadas como informações de Subendereço (como para um subendereço ISDN).                                                                                                                                                                                                                                  |
| *Subendereço*     | Uma cadeia de caracteres de tamanho variavelmente contendo um subendereço. A cadeia de caracteres é delimitada pelo próximo + \| ^ CRLF ou pelo final da cadeia de caracteres de endereço. Ao discar, as informações de Subendereço são passadas para a parte remota. Pode ser para um subendereço ISDN, um endereço de email e assim por diante.                                                                                                                                                                       |
| ^                | Hex (5E) e é opcional. Se estiverem presentes, as informações que o seguem até o próximo CRLF ou o final da cadeia de caracteres de endereço de discagem serão tratadas como um nome ISDN.                                                                                                                                                                                                                                                                                |
| *Nome*           | Uma cadeia de caracteres de tamanho variavelmente tratada como informações de nome. O nome é delimitado por CRLF ou pelo fim da cadeia de caracteres de endereço de discagem. Ao discar, as informações de nome são passadas para a parte remota.                                                                                                                                                                                                                                                      |
| CRLF             | Hex (0D) seguido por Hex (0A). Se estiver presente, esse caractere opcional indicará que outro número de discagem está seguindo este. Ele é usado para separar vários endereços de discagem como parte de uma única cadeia de caracteres de endereço (para multiplexação inversa).                                                                                                                                                                                           |



 

A conversão de endereços pode ser usada para converter um endereço de formato canônico em formato de discagem.

 

