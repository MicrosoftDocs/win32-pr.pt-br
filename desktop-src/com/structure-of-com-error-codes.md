---
title: Estrutura de códigos de erro COM
description: Estrutura de códigos de erro COM
ms.assetid: 97e68708-eb62-4481-af03-cf8b80304103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65953582952ce076028ffcf6652e46356c4cf2afacdd088d546c2fdaafd18a33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104014"
---
# <a name="structure-of-com-error-codes"></a>Estrutura de códigos de erro COM

A ilustração a seguir mostra o formato de [**um HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a) (ou SCODE); os números indicam posições de bit:

![Mostra o formato de um 'H RESULT' ou 'S CODE' com números que indicam posições de bit.](images/a5a947d1-7b5a-4474-afed-2a1c58fe2421.png)

O bit de ordem alta no **HRESULT** ou SCODE indica se o valor de retorno representa êxito ou falha. Se definido como 0, SEVERITY \_ SUCCESS, o valor indicará êxito. Se definido como 1, ERRO DE \_ GRAVIDADE, indica falha.

Os bits R, C, N e r são reservados.

O campo de instalação indica o serviço do sistema responsável pelo erro. A Microsoft aloca novos códigos de instalação conforme eles se tornam necessários. A maioria dos valores SCODEs **e HRESULT** configura o campo de instalação como \_ FACILITY ITF, indicando um erro de método de interface.

Os campos comuns de instalação são descritos na tabela a seguir.



| Campo De instalação                | Valor        | Descrição                                                                                                                                                                                                                                                                                                              |
|-------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXPEDIÇÃO DE \_ INSTALAÇÕES<br/> | 2<br/> | Para erros de interface **IDispatch de** associação tardia. <br/>                                                                                                                                                                                                                                                             |
| \_INSTALAÇÃO ITF<br/>      | 4<br/> | Para a maioria dos códigos de status retornados dos métodos de interface. O significado real do erro é definido pela interface . Ou seja, dois **HRESULT** s com exatamente o mesmo valor de 32 bits retornado de duas interfaces diferentes podem ter significados diferentes. <br/>                                                       |
| RECURSO \_ NULO<br/>     | 0<br/> | Para códigos de status comuns amplamente aplicáveis, como S \_ OK. <br/>                                                                                                                                                                                                                                                    |
| \_INSTALAÇÃO RPC<br/>      | 1<br/> | Para códigos de status retornados de chamadas de procedimento remoto. <br/>                                                                                                                                                                                                                                                       |
| ARMAZENAMENTO DE \_ INSTALAÇÕES<br/>  | 3<br/> | Para códigos de status retornados de chamadas de método [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) relacionadas ao armazenamento estruturado. Códigos de status cujo valor de código (16 bits inferiores) está no intervalo de códigos de erro MS-DOS (ou seja, menor que 256) têm o mesmo significado que o erro MS-DOS correspondente. <br/> |
| INSTALAÇÃO \_ WIN32<br/>    | 7<br/> | Usado para fornecer um meio de lidar com códigos de erro de funções na API Windows como um **HRESULT.** Códigos de erro no OLE de 16 bits que duplicaram códigos de erro do sistema também foram alterados para FACILITY \_ WIN32. <br/>                                                                                                 |
| INSTALAÇÃO \_ DO WINDOWS<br/>  | 8<br/> | Usado para códigos de erro adicionais de interfaces definidas pela Microsoft.<br/>                                                                                                                                                                                                                                            |



 

O campo de código é um número exclusivo atribuído para representar o erro ou aviso.

Por convenção, os **valores HRESULT** geralmente têm nomes no seguinte formato: *Motivo* da \_ *gravidade da* \_ *instalação.*

*O* recurso é o nome do recurso ou algum outro identificador de distinção; *Gravidade é* uma única letra, S ou E, que indica se a chamada de função foi bem-sucedida (S) ou produziu um erro (E); e *Reason* é um identificador que descreve o significado do código. Por exemplo, o código de status STG E FILENOTFOUND indica que ocorreu um erro relacionado ao armazenamento; especificamente, um arquivo solicitado \_ \_ não existe. Os códigos de status de FACILITY \_ NULL omitem o *prefixo De* \_ instalação.

Os códigos de erro são definidos dentro do contexto de uma implementação de interface. Depois de definidos, os códigos de êxito não podem ser alterados ou novos códigos de êxito adicionados. No entanto, novos códigos de falha podem ser gravados. A Microsoft se reserva o direito de definir novos códigos de falha (mas não códigos de êxito) para as interfaces descritas em \_ FACILITY ITF ou em novas instalações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erro em COM](error-handling-in-com.md)
</dt> <dt>

[Windows Protocolos: HRESULT](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)
</dt> </dl>

 

