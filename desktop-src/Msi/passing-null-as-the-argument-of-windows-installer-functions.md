---
description: Windows Installer funções que retornam dados em um usuário fornecido – o local da memória não deve ser chamado com NULL como o valor do ponteiro.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Passando nulo para funções Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb09ceb3982695792614a3c226af9ab276aa3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749788"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a>Passando NULL como o argumento das funções Windows Installer

Windows Installer funções que retornam dados em um usuário fornecido – o local da memória não deve ser chamado com NULL como o valor do ponteiro. Essas funções retornam uma cadeia de caracteres ou retornam dados como ponteiros inteiros, mas retornam valores inconsistentes ao passar NULL como o valor para o argumento de saída.

Não passe nulo como o valor do argumento de saída para qualquer uma das seguintes funções:

[**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



