---
description: O instalador fornece funções que manipulam os registros em um banco de dados de instalação. Essas funções podem ser usadas em conjunto com as funções descritas em trabalhando com consultas para fazer alterações reais em um banco de dados.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Trabalhando com registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3252dc29bf755d08494dbdc2326bf45a4afb1c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748561"
---
# <a name="working-with-records"></a>Trabalhando com registros

O instalador fornece funções que manipulam os registros em um banco de dados de instalação. Essas funções podem ser usadas em conjunto com as funções descritas em [trabalhando com consultas](working-with-queries.md) para fazer alterações reais em um banco de dados.

As funções a seguir criam ou removem registros:

-   Para criar um novo registro para um banco de dados, chame a função [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) .
-   Para limpar dados de um registro, defina cada campo como nulo chamando a função [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) .

As funções a seguir preenchem campos especificados de registros:

-   Para definir um registro como um inteiro, chame a função [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) .
-   Para definir um registro para uma cadeia de caracteres, chame a função [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) .
-   Para inserir um arquivo inteiro em um campo de fluxo, chame a função [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) .

As funções a seguir lêem valores de campos especificados de registros:

-   Para ler um valor inteiro de um campo, chame a função [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) .
-   Para recuperar um valor de cadeia de caracteres, chame a função [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) .
-   Para obter um fluxo, chame a função [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) .
-   Para determinar se um determinado campo de um registro é nulo, chame a função [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) .

As funções a seguir são funções de registro informativo:

-   Para obter o número de campos que um registro contém, chame a função [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) .
-   Para obter o tamanho de um campo, chame a função [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) . O valor de retorno de **MsiRecordDataSize** é sensível ao tipo de campo.

 

 



