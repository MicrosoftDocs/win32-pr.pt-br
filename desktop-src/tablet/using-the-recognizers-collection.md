---
description: Se você usar vários reconhecedores, poderá usar a coleção Recognizers para listar os reconhecedores disponíveis e permitir que um usuário selecione entre eles.
ms.assetid: 1b89def0-3491-42da-9138-5280002e447a
title: Usando a coleção Recognizers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d38625b3c6d4b8ed2475393ba45ae97b5bdc47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754060"
---
# <a name="using-the-recognizers-collection"></a>Usando a coleção Recognizers

Se você usar vários reconhecedores, poderá usar a coleção [**Recognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) para listar os reconhecedores disponíveis e permitir que um usuário selecione entre eles. Uma coleção de **reconhecedores** verifica os reconhecedores instalados, consulta os atributos dos objetos [**reconhecedor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) e armazena os resultados. Os aplicativos podem usar a coleção **Recognizers** para exibir uma lista de reconhecedores disponíveis sem carregar cada DLL de reconhecedor.

> [!Note]  
> A coleção [**Recognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) usa o registro do sistema para verificar os reconhecedores da Microsoft e os reconhecedores de terceiros.

 

A tabela a seguir mostra os valores dos identificadores de idioma compatíveis com cada reconhecedor da Microsoft.

> [!Note]  
> Não há identificadores de idioma associados ao reconhecedor de gestos da Microsoft.

 



| Nome do reconhecedor                                                      | ID do idioma principal, ID do subidioma (em ordem com suporte)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reconhecedor de gestos da Microsoft<br/>                              | Nenhum<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Reconhecedor de manuscrito do Microsoft English (Reino Unido)<br/> | IDIOMA \_ Inglês, subidioma \_ inglês do \_ Reino Unido<br/> idioma \_ Inglês, SUBLANG \_ Inglês \_ Eire<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Reconhecedor de manuscrito do Microsoft English (Estados Unidos)<br/>  | IDIOMA \_ Inglês, SUBLANG \_ Inglês \_ dos EUA<br/> IDIOMA \_ Inglês, SUBLANG \_ Inglês \_ aus<br/> idioma \_ Inglês, meu idioma \_ Inglês ( \_ Belize)<br/> idioma \_ Inglês, o subidioma \_ Inglês \_ pode<br/> IDIOMA \_ Inglês, \_ Caribe inglês (inglês) \_<br/> idioma \_ Inglês, Jamaica do subidioma \_ Inglês \_<br/> idioma \_ Inglês, \_ NZ em inglês de SUBLANG \_<br/> idioma \_ Inglês, \_ Filipinas inglês (SUBLANG) \_<br/> IDIOMA \_ Inglês, subidioma \_ Inglês \_ do Sul da \_ África<br/> IDIOMA \_ Inglês, \_ Trinidad inglês e Inglês \_<br/> idioma \_ Inglês, \_ Zimbábue inglês de subidioma \_<br/> idioma \_ Inglês, neutro em SUBidioma \_<br/> |
| Reconhecedor de manuscrito em francês da Microsoft<br/>                   | IDIOMA \_ francês, subidioma \_ francês<br/> IDIOMA \_ francês, Bélgica do idioma \_ francês \_<br/> IDIOMA \_ francês, \_ \_ Canadá francês canadense<br/> IDIOMA \_ francês, \_ Luxemburgo francês de subidioma \_<br/> IDIOMA \_ francês, o subidioma \_ francês \_ Mônaco<br/> IDIOMA \_ francês, subidioma \_ francês \_ suíço<br/> IDIOMA \_ francês, \_ neutro<br/>                                                                                                                                                                                                                                                                                     |
| Reconhecedor de manuscrito em alemão da Microsoft<br/>                   | IDIOMA \_ alemão, subidioma \_ alemão<br/> LANG \_ alemão, subidioma \_ alemão \_ austríaco<br/> LANG \_ alemão, SUBLANG \_ alemão \_ Liechtenstein<br/> LANG \_ alemão, SUBLANG \_ alemão \_ Luxemburgo<br/> LANG \_ alemão, subidioma \_ alemão \_ suíço<br/> LANG \_ alemão, SUBLANG \_ neutro<br/>                                                                                                                                                                                                                                                                                                                                |
| Reconhecedor de manuscrito em espanhol da Microsoft<br/>                  | IDIOMA \_ espanhol, subidioma \_ espanhol<br/> IDIOMA \_ espanhol, neutro em SUBidioma \_<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Reconhecedor de manuscrito japonês da Microsoft<br/>                 | IDIOMA \_ japonês, neutro em SUBidioma \_<br/> IDIOMA \_ japonês, padrão de SUBidioma \_<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Reconhecedor de manuscrito coreano da Microsoft<br/>                   | LANG \_ coreano, SUBLANG \_ neutro<br/> IDIOMA \_ coreano, padrão de SUBidioma \_<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Reconhecedor de manuscrito do Microsoft chinês (simplificado)<br/>     | IDIOMA \_ chinês, subidioma \_ chinês \_ simplificado<br/> IDIOMA \_ chinês, subidioma \_ chinês \_ Cingapura<br/> IDIOMA \_ chinês, neutro em SUBidioma \_<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Reconhecedor de manuscrito do Microsoft chinês (tradicional)<br/>    | IDIOMA \_ chinês, subidioma \_ chinês \_ tradicional<br/> IDIOMA \_ chinês, subidioma \_ chinês \_ Hong Kong<br/> IDIOMA \_ chinês, Macau, \_ chinês-idioma \_<br/> IDIOMA \_ chinês, neutro em SUBidioma \_<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

Para obter mais informações sobre identificadores de idioma, consulte [constantes e cadeias de caracteres de identificador de linguagem](../intl/language-identifier-constants-and-strings.md).

 

 
