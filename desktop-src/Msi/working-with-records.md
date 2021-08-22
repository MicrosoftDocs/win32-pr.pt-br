---
description: O instalador fornece funções que manipulam os registros em um banco de dados de instalação. Essas funções podem ser usadas em conjunto com as funções descritas em Trabalhando com consultas para fazer alterações reais em um banco de dados.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Trabalhando com registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f83159688ec106b8e3cea3021e4352c851620d0e2f89661cee823c1439c120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498376"
---
# <a name="working-with-records"></a>Trabalhando com registros

O instalador fornece funções que manipulam os registros em um banco de dados de instalação. Essas funções podem ser usadas em conjunto com as funções descritas em Trabalhando com consultas [para](working-with-queries.md) fazer alterações reais em um banco de dados.

As seguintes funções criam ou removem registros:

-   Para criar um novo registro para um banco de dados, chame a [**função MsiCreateRecord.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)
-   Para limpar dados de um registro, de definir cada campo como nulo chamando a [**função MsiRecordClearData.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)

As seguintes funções preenchem campos de registros especificados:

-   Para definir um registro como um inteiro, chame a [**função MsiRecordSetInteger.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)
-   Para definir um registro como uma cadeia de caracteres, chame a [**função MsiRecordSetString.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)
-   Para inserir um arquivo inteiro em um campo de fluxo, chame a [**função MsiRecordSetStream.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)

As seguintes funções leem valores de campos de registros especificados:

-   Para ler um valor inteiro de um campo, chame a [**função MsiRecordGetInteger.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)
-   Para recuperar um valor de cadeia de [**caracteres, chame a função MsiRecordGetString.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)
-   Para obter um fluxo, chame a [**função MsiRecordReadStream.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)
-   Para determinar se um campo específico de um registro é nulo, chame a [**função MsiRecordIsNull.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)

As seguintes funções são funções de registro informativas:

-   Para obter o número de campos que um registro contém, chame a [**função MsiRecordGetFieldCount.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount)
-   Para obter o tamanho de um campo, chame a [**função MsiRecordDataSize.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) O valor de retorno **de MsiRecordDataSize** é sensível ao tipo de campo.

 

 



