---
title: Estrutura de códigos de erro COM
description: Estrutura de códigos de erro COM
ms.assetid: 97e68708-eb62-4481-af03-cf8b80304103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb27143f50028592f6fe0aeb5cab9795dcd10d4a
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104570653"
---
# <a name="structure-of-com-error-codes"></a>Estrutura de códigos de erro COM

A ilustração a seguir mostra o formato de um [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a) (ou SCODE); os números indicam as posições de bits:

![Mostra o formato de um "resultado" ou "código" com números que indicam posições de bits.](images/a5a947d1-7b5a-4474-afed-2a1c58fe2421.png)

O bit de ordem superior no **HRESULT** ou SCODE indica se o valor de retorno representa êxito ou falha. Se definido como 0, \_ êxito na severidade, o valor indica êxito. Se definido como 1, erro de severidade \_ , indica falha.

Os bits R, C, N e R são reservados.

O campo recurso indica o serviço do sistema responsável pelo erro. A Microsoft aloca novos códigos de recursos à medida que eles se tornam necessários. A maioria dos valores SCODEs e **HRESULT** definem o campo recurso como recurso \_ ITF, indicando um erro de método de interface.

Os campos de recursos comuns são descritos na tabela a seguir.



| Campo de recurso                | Valor        | Descrição                                                                                                                                                                                                                                                                                                              |
|-------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| expedição de recursos \_<br/> | 2<br/> | Para erros da interface **IDispatch** de ligação tardia. <br/>                                                                                                                                                                                                                                                             |
| ITF de instalação \_<br/>      | 4<br/> | Para a maioria dos códigos de status retornados dos métodos de interface. O significado real do erro é definido pela interface. Ou seja, dois **HRESULT** s com exatamente o mesmo valor de 32 bits retornado de duas interfaces diferentes podem ter significados diferentes. <br/>                                                       |
| RECURSO \_ nulo<br/>     | 0<br/> | Para códigos de status comuns amplamente aplicáveis, como S \_ OK. <br/>                                                                                                                                                                                                                                                    |
| RECURSO \_ RPC<br/>      | 1<br/> | Para códigos de status retornados de chamadas de procedimento remoto. <br/>                                                                                                                                                                                                                                                       |
| armazenamento de instalações \_<br/>  | 3<br/> | Para códigos de status retornados das chamadas de método [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) relacionadas ao armazenamento estruturado. Os códigos de status cujo valor de código (mais de 16 bits) está no intervalo de códigos de erro do MS-DOS (ou seja, menos de 256) têm o mesmo significado que o erro do MS-DOS correspondente. <br/> |
| RECURSO \_ Win32<br/>    | 7<br/> | Usado para fornecer um meio de manipular códigos de erro de funções na API do Windows como um **HRESULT**. Os códigos de erro em OLE de 16 bits que códigos de erro duplicados do sistema também foram alterados para recursos do \_ Win32. <br/>                                                                                                 |
| janelas de instalações \_<br/>  | 8<br/> | Usado para códigos de erro adicionais das interfaces definidas pela Microsoft.<br/>                                                                                                                                                                                                                                            |



 

O campo de código é um número exclusivo que é atribuído para representar o erro ou aviso.

Por convenção, os valores **HRESULT** geralmente têm nomes no seguinte formato:  \_ motivo de *gravidade* da instalação \_ .

O *recurso* é o nome do recurso ou algum outro identificador diferencial; *Severidade* é uma única letra, S ou e, que indica se a chamada de função foi bem-sucedida ou produziu um erro (E); e o *motivo* é um identificador que descreve o significado do código. Por exemplo, o código de status STG \_ E \_ FILENOTFOUND indica que ocorreu um erro relacionado ao armazenamento; especificamente, um arquivo solicitado não existe. Os códigos de status do recurso \_ NULL omitem o prefixo de *recurso* \_ .

Os códigos de erro são definidos dentro do contexto de uma implementação de interface. Uma vez definidas, os códigos de êxito não podem ser alterados ou novos códigos de êxito foram adicionados. No entanto, novos códigos de falha podem ser gravados. A Microsoft se reserva o direito de definir novos códigos de falha (mas não códigos de êxito) para as interfaces descritas em FACILITy \_ ITF ou em novas instalações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erro em COM](error-handling-in-com.md)
</dt> <dt>

[Protocolos do Windows: HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)
</dt> </dl>

 

