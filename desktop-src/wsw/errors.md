---
title: Erros
description: Esta seção descreve o erro que pode ser Windows funções de Serviços Web em resultado de uma falha ao executar o comando.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Erros de Serviços Web para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a08a6371dcc5265239c6a25ce0c01075cff3ae12533862ed8a1cbbbe7aba705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026524"
---
# <a name="errors"></a>Erros

Esta seção descreve o erro que pode ser Windows funções de Serviços Web em resultado de uma falha ao executar o comando.

-   [Parâmetros de saída](#out-parameters)
-   [Códigos de Erro](#error-codes)
-   [Erros de rich](#rich-errors)
-   [Falhas e erros](#faults-and-errors)
-   [Informações de erro sensíveis ao idioma](#language-sensitive-error-information)
-   [Códigos de erro canônicos](#canonical-error-codes)
-   [Uso inválido de API](#invalid-api-usage)
-   [Segurança](#security)

## <a name="out-parameters"></a>Parâmetros de saída

Como regra geral, o valor de parâmetros out não será modificado se uma função falhar.

Há algumas instâncias em que os parâmetros out são modificados se a função falhar. Esses casos são explicitamente chamados na documentação de cada parâmetro. Se a documentação não mencionar nada sobre como modificar parâmetros em caso de falha, você poderá presumir com segurança que a função não os modificará.

## <a name="error-codes"></a>Códigos de erro

Todos os códigos de retorno de erro são HRESULTs. Essa API define um conjunto de HRESULTs no intervalo FACILITY WEBSERVICES, mas também retorna erros definidos em outro lugar na \_ API Windows.

Consulte a documentação de APIs específicas para saber quais códigos de erro são retornados. A lista não se destina a ser exaustiva para cada API, mas sim uma lista de códigos de erro para os quais há cenários comuns para tratamento explícito. Um chamador sempre deve assumir que outros códigos de erro são possíveis de qualquer API.

Essa API define um número relativamente pequeno de códigos de erro, que correspondem a cenários em que um programa deseja tomar medidas com base no erro. Os códigos de erro sozinhos podem não ser suficientes para determinar o que deu errado ou para fornecer uma boa descrição do problema para o usuário. A melhor compreensão do problema vem do uso de Erros Rich, conforme descrito abaixo.

## <a name="rich-errors"></a>Erros de rich

Além de retornar um código de erro, um chamador pode, opcionalmente, solicitar informações de erro rich para qualquer chamada à API passando um objeto ERROR [WS \_ não](ws-error.md) **NULL.** Para criar um objeto de erro, use [**WsCreateError.**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror) Se houver um erro, a API que causou o erro preencherá o objeto de erro com contexto adicional sobre a situação de erro. Se não houver nenhum erro, o objeto de erro não será modificado. Passar um **objeto de** erro NULL indica que o chamador não está interessado em informações de erro rich. Os chamados (incluindo retornos de chamada) devem estar preparados para lidar com objetos de erro **NULL.**

Observe que o mesmo objeto de erro pode ser usado para várias chamadas à API, mas só pode ser usado para uma chamada à API por vez (pois é single threaded). Sempre que ocorre um erro, as informações de erro são anexadas ao objeto de erro. À medida que uma cadeia de chamada desenrola, várias funções podem adicionar informações ao objeto de erro para fornecer contexto adicional sobre o erro. Para limpar o conteúdo do objeto de erro antes de reutilizá-lo (após ocorrer um erro), use [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror). Se nenhum erro ocorrer, não será necessário redefinir o objeto de erro antes de reutilizá-lo.

As informações de erro rich consistem no seguinte:

-   Um conjunto de valores de propriedade, que fornecem informações adicionais sobre o erro, se presente. Consulte [**PROPRIEDADE DE ERRO \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).
-   Zero ou mais cadeias de caracteres de erro. As cadeias de caracteres são [**adicionadas usando WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)e podem ser consultadas usando [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring). O número de cadeias de caracteres pode ser consultado usando [**WS \_ ERROR PROPERTY STRING \_ \_ \_ COUNT**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="faults-and-errors"></a>Falhas e erros

Consulte [Falhas para](faults.md) obter informações sobre como erros e falhas se relacionam.

## <a name="language-sensitive-error-information"></a>Informações de erro sensíveis ao idioma

Ao criar um objeto de erro, a LANGID da tradução de idioma desejada para informações de erro é especificada. Isso é usado ao adicionar informações de erro ao objeto de erro.

Esse valor de linguagem pode ser recuperado ou definido usando [**WS \_ ERROR PROPERTY \_ \_ LANGID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="canonical-error-codes"></a>Códigos de erro canônicos

Essa API fornece um conjunto canônico de códigos de erro (WS E ) que permitem que diferentes tecnologias de comunicação sejam usadas sem precisar depender dos códigos de erro específicos da implementação subjacente \_ \_ \* específica. Para ver uma lista completa desses códigos de erro, consulte Windows valores de [retorno dos Serviços Web.](windows-web-services-return-values.md)

Isso permite, por exemplo, que um programa verifique o código de erro **WS \_ E \_ ENDPOINT \_ NOT \_ FOUND** usando TCP, UDP ou HTTP e tome alguma ação (como tentar usar um ponto de extremidade diferente).

Quando um código de erro específico de implementação é mapeado para um erro canônico, o código de erro original é salvo no objeto de erro e ainda pode ser acessado para fins de diagnóstico. Consulte [**WS \_ ERROR PROPERTY ORIGINAL ERROR CODE \_ \_ \_ \_ para**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) obter mais informações.

## <a name="invalid-api-usage"></a>Uso inválido de API

Os códigos de erro a seguir são reservados para uso inválido da API e não serão retornados em outras circunstâncias. Se qualquer um desses erros for retornado, poderá ser uma indicação de um bug de aplicativo.

-   **OPERAÇÃO INVÁLIDA DO WS \_ E \_ \_**
-   **E \_ INVALIDARG**

As enumerações a seguir fazem parte do rastreamento:

-   [**ID DA \_ \_ PROPRIEDADE DE ERRO \_ do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**CÓDIGO DE \_ EXCEÇÃO DO WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

Os seguintes códigos de erro fazem parte do rastreamento:

-   **CERT \_ E \_ CN \_ NO \_ MATCH**
-   **CERTIFICADO \_ E \_ EXPIRADO**
-   **CERT \_ E \_ UNTRUSTEDROOT**
-   **CERT \_ E \_ USO \_ ERRADO**
-   **REVOGAÇÃO \_ \_ DE CRIPTOGRAFIA \_ OFFLINE**
-   **E \_ INVALIDARG**
-   **E \_ OUTOFMEMORY**
-   **ENDEREÇO WS \_ E \_ EM \_ \_ USO**
-   **ENDEREÇO WS \_ \_ E NÃO \_ \_ DISPONÍVEL**
-   **ACESSO AO PONTO DE EXTREMIDADE DO WS \_ \_ E \_ \_ NEGADO**
-   **NÃO HÁ SUPORTE PARA A AÇÃO DE PONTO DE \_ \_ EXTREMIDADE \_ \_ \_ DO WS E**
-   **PONTO DE \_ EXTREMIDADE \_ WS E \_ DESCONECTADO**
-   **FALHA DO PONTO DE EXTREMIDADE DO WS \_ E \_ \_**
-   **FALHA DE \_ \_ PONTO DE EXTREMIDADE \_ WS E \_ RECEBIDA**
-   **PONTO \_ DE \_ EXTREMIDADE WS E \_ NÃO \_ DISPONÍVEL**
-   **PONTO DE \_ EXTREMIDADE WS E \_ NÃO \_ \_ ENCONTRADO**
-   **PONTO DE \_ EXTREMIDADE WS E \_ MUITO \_ \_ OCUPADO**
-   **PONTO \_ DE EXTREMIDADE WS E \_ \_ INACESSÍVEL**
-   **URL \_ DE PONTO \_ DE EXTREMIDADE \_ INVÁLIDA DO \_ WS E**
-   **WS \_ E \_ FORMATO \_ INVÁLIDO**
-   **OPERAÇÃO INVÁLIDA DO WS \_ E \_ \_**
-   **WS \_ E \_ SEM \_ SUPORTE**
-   **WS \_ E \_ NO \_ TRANSLATION \_ AVAILABLE**
-   **WS \_ E \_ NUMERIC \_ OVERFLOW**
-   **OBJETO WS \_ E \_ COM \_ FALHA**
-   **OPERAÇÃO WS \_ E \_ \_ ABANDONADA**
-   **OPERAÇÃO WS \_ E \_ \_ ANULADA**
-   **A OPERAÇÃO \_ WS \_ E FOI O TEMPO DE \_ \_ VIDA**
-   **WS \_ E \_ OTHER**
-   **ACESSO DE PROXY DO WS \_ E \_ \_ \_ NEGADO**
-   **FALHA DE PROXY DO WS \_ E \_ \_**
-   **O \_ PROXY WS E \_ \_ REQUER \_ \_ AUTH BÁSICA**
-   **o \_ proxy WS E \_ \_ requer \_ \_ autenticação Digest**
-   **o \_ proxy WS E \_ \_ requer \_ Negotiate \_ auth**
-   **o \_ proxy WS E \_ \_ requer \_ \_ autenticação NTLM**
-   **cota de WS \_ E \_ \_ excedida**
-   **\_ \_ \_ falha no sistema de segurança WS E \_**
-   **TOKEN de segurança do WS \_ E \_ \_ \_ expirado**
-   **\_ \_ \_ falha na verificação de segurança do WS E \_**
-   **o \_ WS \_ E \_ Server \_ requer \_ autenticação básica**
-   **o \_ WS \_ E \_ Server \_ requer \_ autenticação Digest**
-   **o WS \_ E \_ Server \_ requer \_ Negotiate \_ auth**
-   **o \_ WS \_ E \_ Server \_ requer \_ autenticação NTLM**
-   **WS \_ S \_ Async**
-   **fim do WS- \_ S \_**

As funções a seguir fazem parte do rastreamento:

-   [**\_ID da \_ propriedade de erro WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**\_código de exceção WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

O seguinte identificador é parte do rastreamento:

-   [\_erro WS](ws-error.md)

A seguinte estrutura faz parte do rastreamento:

-   [**\_propriedade de erro WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a>Segurança

Há várias considerações de segurança que o usuário do objeto de erro deve estar ciente:

-   O objeto de erro pode conter dados não confiáveis. Exemplos disso são: a falha do WS \_ e as cadeias de caracteres de erro, que podem ser armazenadas no objeto de erro com base nas informações recebidas por um canal não confiável. O usuário do objeto de erro deve ser cuidadoso ao inspecionar as informações no objeto de erro e tomar decisões com base em seus valores.
-   Um usuário do objeto de erro deve chamar [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) depois de inspecionar as informações sobre o erro. A falha ao fazer isso pode levar à acumulação de memória.
-   Um usuário do objeto de erro deve ser muito cuidadoso ao usar o \_ valor de \_ \_ divulgação de falha completa do WS da enumeração de [**\_ \_ divulgação de falha do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) , pois a falha gerada pode conter informações privadas que foram acumuladas como parte do processo de gravação de erros.

 

 




