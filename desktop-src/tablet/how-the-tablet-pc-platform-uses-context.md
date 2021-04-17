---
description: Os desenvolvedores que criam aplicativos para o Tablet PC podem tirar proveito das informações de escopo e contexto de entrada.
ms.assetid: 74e4e4b2-6ceb-4044-84df-2fff0788267a
title: Como a plataforma Tablet PC usa o contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd991a2ad8e76bb0a96ea5e41977b158cc30f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752586"
---
# <a name="how-the-tablet-pc-platform-uses-context"></a>Como a plataforma Tablet PC usa o contexto

Os desenvolvedores que criam aplicativos para o Tablet PC podem tirar proveito das informações de escopo e contexto de entrada. As melhores soluções possíveis para definir informações de contexto sobre controles em aplicativos dependem de se o controle está habilitado para tinta e se o aplicativo foi lançado no mercado. Um controle habilitado para tinta é aquele criado especificamente para entrada à tinta e na qual os dados de tinta são coletados principalmente e mantidos como tinta. Exemplos de aplicativos habilitados para tinta são o diário do Microsoft Windows ou um programa de esboços. Em um controle que não está habilitado para tinta, os dados de entrada são coletados e mantidos como texto, normalmente usando o painel de entrada do Tablet PC quando o aplicativo é executado em um Tablet PC. As soluções para habilitar informações de contexto dentro de controles são:

-   As APIs [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) : uma solução programática de baixo nível para aplicativos e controles não habilitados para tinta. Os binários do aplicativo são afetados e devem ser redistribuídos.
-   As propriedades de [**facto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) e lista de [**palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) : uma solução programática para aplicativos com controles que são habilitados para tinta. Os binários do aplicativo são afetados e devem ser redistribuídos.

O painel de entrada do Tablet PC foi atualizado a partir do Windows Vista para aproveitar as informações de contexto que você fornece ao usar as APIs [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) . A tabela a seguir fornece detalhes sobre quais mecanismos de reconhecimento da Microsoft dão suporte a quais escopos de entrada. Um "X" na linha de um escopo de entrada indica que o reconhecedor nessa coluna dá suporte ao escopo de entrada.



| Nome da Propriedade                                     | Inglês (Estados Unidos) | Inglês (Reino Unido) | Alemão       | Francês       | Japonês     | Coreano       | Chinês (Simplificado) | Chinês (Tradicional) |
|---------------------------------------------------|-------------------------|--------------------------|--------------|--------------|--------------|--------------|----------------------|-----------------------|
| **é \_ endereço \_ FULLPOSTALADDRESS**<br/>     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ endereço \_ POSTALCODE**<br/>            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ rua do endereço \_**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ endereço \_ EstadoOuProvíncia**<br/>       | X<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ cidade do endereço \_**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ endereço \_ countryname**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ endereço \_ COUNTRYSHORTNAME**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ AMOUNTANDSYMBOL de moeda \_**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ valor da moeda \_**<br/>               | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ data de \_ FULLDATE**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ mês de data \_**<br/>                    | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ dia de data \_**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ ano de data \_**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ data de \_ MONTHNAME**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ data de \_ DAYNAME**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ padrão**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ email \_ nome de usuário**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ SMTPEMAILADDRESS de email \_**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ arquivo \_ FULLFILEPATH**<br/>             | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ nome do arquivo \_**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ LoginName**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ dígitos**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ número**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ ONECHAR**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ senha**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ personalname \_ FullName**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ prefixo personalname \_**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ pessoalname \_ fornecido**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é um \_ \_ middlewarename pessoal**<br/>       | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ pessoalname \_ sobrenome**<br/>          | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ sufixo personalname \_**<br/>           | X<br/>            | -<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ telefone \_ FULLTELEPHONENUMBER**<br/> | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ telefone \_ COUNTRYCODE**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ telefone \_ AREACODE**<br/>            | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ telefone \_ LOCALNUMBER**<br/>         | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ tempo \_ FullTime**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ hora de hora \_**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ hora de \_ MINORSEC**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ URL**<br/>                            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ número de \_ largura total**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **TEM \_ \_ metade alfanumérica**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ alfanumérico de \_ largura**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ chinês-moeda \_**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ bopomofo**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ Hiragana**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ de \_ meia-katakana**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ Katakana de \_ largura**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **é \_ Hanja**<br/>                          | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |



 

Ao usar as APIs [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) ou a propriedade [**factoname**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) para definir o contexto, a tentativa de definir um escopo de entrada para um idioma sem suporte pelo reconhecedor desse idioma faz com que o painel de entrada do Tablet PC use o modelo de idioma padrão como o contexto do controle. Por exemplo, não há suporte para o escopo de entrada **\_ \_ EstadoOuProvíncia de endereço** no reconhecedor francês. Se você definir o contexto em um campo como

`(!IS_ADDRESS_STATEORPROVINCE)|(!IS_ADDRESS_POSTALCODE)`

ao usar o reconhecedor francês, o contexto resultante é o modelo de idioma padrão. Para evitar esse problema, detecte o idioma do reconhecedor em uso e defina os escopos de entrada de acordo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumeração InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)
</dt> </dl>

 

