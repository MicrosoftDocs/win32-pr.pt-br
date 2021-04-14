---
title: Estratégias de tratamento de erros
description: Estratégias de tratamento de erros
ms.assetid: 8d03ede8-0661-43dc-adaf-3c1f5fc1687e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c594a8b1e5baf0eab3d928b8f1b861b7f0160d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "104453838"
---
# <a name="error-handling-strategies"></a>Estratégias de tratamento de erros

Como os métodos de interface são virtuais, não é possível que um chamador conheça o conjunto completo de valores que podem ser retornados de qualquer chamada. Uma implementação de um método pode retornar cinco valores; outra pode retornar oito.

A documentação lista os valores comuns que podem ser retornados para cada método; Esses são os valores que você deve verificar e manipular em seu código, pois eles têm significados especiais. Outros valores podem ser retornados, mas como não são significativos, você não precisa escrever código especial para tratá-los. Uma verificação simples de zero ou diferente de 0 é adequada.

## <a name="hresult-values"></a>Valores HRESULT

O valor de retorno de funções e métodos COM é um **HRESULT**. Os valores de alguns HRESULTs foram alterados em COM para eliminar toda a duplicação e sobreposição com os códigos de erro do sistema. Aqueles que duplicam códigos de erro do sistema foram alterados para o \_ Win32 do recurso e aqueles que se sobrepõem permanecem em instalações \_ nulas. Os valores **HRESULT** comuns e seus valores são listados na tabela a seguir.



| HRESULT                    | Valor                 | Descrição                                                                                                                                        |
|----------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| E \_ anular<br/>        | 0x80004004<br/> | A operação foi anulada devido a um erro não especificado.<br/>                                                                              |
| E \_ ACCESSDENIED<br/> | 0x80070005<br/> | Um erro geral de acesso negado.<br/>                                                                                                          |
| E \_ falha<br/>         | 0x80004005<br/> | Ocorreu uma falha não especificada.<br/>                                                                                                    |
| \_identificador E<br/>       | 0x80070006<br/> | Um identificador inválido foi usado.<br/>                                                                                                             |
| E \_ INVALIDARG<br/>   | 0x80070057<br/> | Um ou mais argumentos são inválidos.<br/>                                                                                                      |
| E \_ NOinterface<br/>  | 0x80004002<br/> | O método [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) não reconheceu a interface solicitada. Não há suporte para a interface.<br/> |
| E \_ NOTIMPL<br/>      | 0x80004001<br/> | O método não está implementado.<br/>                                                                                                          |
| E \_ OUTOFMEMORY<br/>  | 0x8007000E<br/> | O método não alocou a memória necessária.<br/>                                                                                         |
| E \_ pendente<br/>      | 0x8000000A<br/> | Os dados necessários para concluir a operação ainda não estão disponíveis.<br/>                                                                      |
| \_ponteiro E<br/>      | 0x80004003<br/> | Foi usado um ponteiro inválido.<br/>                                                                                                            |
| E \_ inesperado<br/>   | 0x8000FFFF<br/> | Ocorreu uma falha catastrófica.<br/>                                                                                                    |
| \_falso<br/>        | 0x00000001<br/> | O método foi bem-sucedido e retornou o valor booliano **false**.<br/>                                                                          |
| S \_ OK<br/>           | 0x00000000<br/> | O método foi bem-sucedido. Se um valor de retorno booliano for esperado, o valor retornado será **true**.<br/>                                            |



 

## <a name="network-errors"></a>Erros de rede

Se os quatro primeiros dígitos do código de erro forem 8007, isso indicará um erro de sistema ou de rede. Você pode usar o comando **net** para decodificar esses tipos de erros. Para decodificar o erro, primeiro converta os últimos quatro dígitos do código de erro hexadecimal em decimal. Em seguida, no prompt de comando, digite o seguinte, em que o código decimal é substituído pelo valor de retorno que você deseja decodificar:

**NET HELPMSG <***\_ código decimal***>**

O comando net retorna uma descrição do erro. Por exemplo, se COM retornar o erro 8007054B, converta o 054B para decimal (1355). Depois, digite o seguinte:

**NET HELPMSG 1355**

O comando net retorna a descrição do erro: "o domínio especificado não existia".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erro em COM](error-handling-in-com.md)
</dt> </dl>

 

 





