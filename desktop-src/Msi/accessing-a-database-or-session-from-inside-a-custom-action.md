---
description: Você não pode acessar uma sessão do instalador de uma ação personalizada que não seja a sessão de instalação atual.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Acessando um banco de dados ou sessão de dentro de uma ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c653d14bc2fdb361469389c4ee053e5d98b65f8c8265516c4e2c3bd4fc4c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046056"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a>Acessando um banco de dados ou sessão de dentro de uma ação personalizada

Você não pode acessar uma sessão do instalador de uma ação personalizada que não seja a sessão de instalação atual. As ações personalizadas são limitadas a trabalhar apenas com o banco de dados ativo da sessão e nenhum outro banco de dados. As seguintes Windows Funções [](database-functions.md) de Banco de Dados do Instalador não devem ser chamadas de uma ação personalizada, pois exigem um handle para um banco de dados que não é o banco de dados da sessão de instalação atual:

[**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando a sessão do instalador atual de dentro de uma ação personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



