---
description: A ação InstallAdminPackage copia o banco de dados do produto para o ponto de instalação administrativa, que é definido pela propriedade TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Ação InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921477"
---
# <a name="installadminpackage-action"></a>Ação InstallAdminPackage

A ação InstallAdminPackage copia o banco de dados do produto para o ponto de instalação administrativa, que é definido pela propriedade [**TARGETDIR**](targetdir.md) .

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                                 |
|-------|------------------------------------------------------------|
| \[1\] | Nome dos arquivos de instalação.                                     |
| \[6\] | Tamanho do banco de dados.                                          |
| \[9\] | Identificador de instalação administrativa – diretório de ponto. |



 

## <a name="remarks"></a>Comentários

A ação InstallAdminPackage também atualiza as informações de resumo do banco de dados e remove os arquivos de gabinete localizados em fluxos depois que o banco de dados é copiado.

 

 



