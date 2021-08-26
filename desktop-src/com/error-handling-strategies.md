---
title: Estratégias de tratamento de erros
description: Estratégias de tratamento de erros
ms.assetid: 8d03ede8-0661-43dc-adaf-3c1f5fc1687e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0527edbb8bab4b4a0b0ca9e0d135bc5cf8c2827497a36fb9cad021680868f764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029966"
---
# <a name="error-handling-strategies"></a>Estratégias de tratamento de erros

Como os métodos de interface são virtuais, não é possível que um chamador saiba o conjunto completo de valores que podem ser retornados de qualquer chamada. Uma implementação de um método pode retornar cinco valores; outro pode retornar oito.

A documentação lista valores comuns que podem ser retornados para cada método; esses são os valores que você deve verificar e manipular em seu código porque eles têm significados especiais. Outros valores podem ser retornados, mas como eles não são significativos, você não precisa escrever código especial para lidar com eles. Uma verificação simples de zero ou não zero é adequada.

## <a name="hresult-values"></a>Valores HRESULT

O valor de retorno de funções e métodos COM é um **HRESULT.** Os valores de alguns HRESULTs foram alterados em COM para eliminar toda a duplicação e sobreposição com os códigos de erro do sistema. Aqueles que duplicam códigos de erro do sistema foram alterados para FACILITY WIN32 e aqueles que se sobrepõem \_ permanecem em FACILITY \_ NULL. Os valores comuns de **HRESULT** e seus valores são listados na tabela a seguir.



| HRESULT                    | Valor                 | Descrição                                                                                                                                        |
|----------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| E \_ ABORT<br/>        | 0x80004004<br/> | A operação foi anulada devido a um erro não especificado.<br/>                                                                              |
| E \_ ACCESSDENIED<br/> | 0x80070005<br/> | Um erro de acesso negado geral.<br/>                                                                                                          |
| E \_ FAIL<br/>         | 0x80004005<br/> | Ocorreu uma falha não especificada.<br/>                                                                                                    |
| E \_ HANDLE<br/>       | 0x80070006<br/> | Um alça inválido foi usado.<br/>                                                                                                             |
| E \_ INVALIDARG<br/>   | 0x80070057<br/> | Um ou mais argumentos são inválidos.<br/>                                                                                                      |
| E \_ NOINTERFACE<br/>  | 0x80004002<br/> | O [**método QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) não reconheceu a interface solicitada. Não há suporte para a interface .<br/> |
| E \_ NOTIMPL<br/>      | 0x80004001<br/> | O método não é implementado.<br/>                                                                                                          |
| E \_ OUTOFMEMORY<br/>  | 0x8007000E<br/> | O método não conseguiu alocar a memória necessária.<br/>                                                                                         |
| E \_ PENDENTE<br/>      | 0x8000000A<br/> | Os dados necessários para concluir a operação ainda não estão disponíveis.<br/>                                                                      |
| PONTEIRO \_ E<br/>      | 0x80004003<br/> | Um ponteiro inválido foi usado.<br/>                                                                                                            |
| E \_ UNEXPECTED<br/>   | 0x8000FFFF<br/> | Ocorreu uma falha catastrófica.<br/>                                                                                                    |
| S \_ FALSE<br/>        | 0x00000001<br/> | O método foi bem-sucedido e retornou o valor **booliana FALSE.**<br/>                                                                          |
| S \_ OK<br/>           | 0x00000000<br/> | O método foi bem-sucedido. Se um valor retornado booliana for esperado, o valor retornado será **TRUE.**<br/>                                            |



 

## <a name="network-errors"></a>Erros de rede

Se os primeiros quatro dígitos do código de erro são 8007, isso indica um erro de sistema ou rede. Você pode usar o **comando net** para decodificar esses tipos de erros. Para decodificar o erro, primeiro converta os últimos quatro dígitos do código de erro hexadecimal em decimal. Em seguida, no prompt de comando, digite o seguinte, em que o código decimal é substituído pelo valor de retorno que você deseja decodificar:

**net helpmsg <** _código \_ decimal_*_>_*

O comando net retorna uma descrição do erro. Por exemplo, se COM retornar o erro 8007054B, converta o 054B em decimal (1355). Depois, digite o seguinte:

**net helpmsg 1355**

O comando net retorna a descrição do erro: "O domínio especificado não existia".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erro em COM](error-handling-in-com.md)
</dt> </dl>

 

 





