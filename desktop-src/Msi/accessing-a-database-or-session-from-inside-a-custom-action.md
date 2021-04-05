---
description: Não é possível acessar uma sessão de instalador de uma ação personalizada que não seja a sessão de instalação atual.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Acessando um banco de dados ou sessão de dentro de uma ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921538"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a>Acessando um banco de dados ou sessão de dentro de uma ação personalizada

Não é possível acessar uma sessão de instalador de uma ação personalizada que não seja a sessão de instalação atual. As ações personalizadas são limitadas a trabalhar apenas com o banco de dados ativo da sessão e nenhum outro. As funções de [banco de dados](database-functions.md) a seguir Windows Installer não devem ser chamadas de uma ação personalizada, porque exigem um identificador para um banco de dados que não seja o banco de dados da sessão de instalação atual:

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

 

 



