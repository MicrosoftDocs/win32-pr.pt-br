---
description: O ICE73 verifica se o pacote não reutiliza códigos de pacote, códigos de atualização ou códigos de produto dos exemplos do SDK Windows Installer. Os pacotes nunca devem reutilizar o pacote, a atualização ou os códigos de produto de outro produto.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e5beecbfc7b4345d3b0dd7a93b86c55acc1abde4cc4f99d72749368be9d303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635069"
---
# <a name="ice73"></a>ICE73

O ICE73 verifica se o pacote não reutiliza códigos de pacote, códigos de atualização ou códigos de produto dos exemplos do SDK Windows Installer. Os pacotes nunca devem reutilizar o pacote, a atualização ou os códigos de produto de outro produto.

## <a name="result"></a>Resultado

O ICE73 emite um aviso se o pacote do seu produto reutiliza um código de pacote ou produto de um Windows SDK do Instalador.

## <a name="example"></a>Exemplo

O ICE73 relata os seguintes erros para o exemplo mostrado:

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> Os asteriscos ( ) no GUID representam o intervalo de GUIDs reservados para pacotes \* \* \* \* do SDK Windows Instalador subsequentes.

 

Para corrigir os erros, gere um novo GUID exclusivo para os códigos de produto e pacote do pacote. Você também precisará de um novo GUID exclusivo para o código de atualização do pacote.

[Fluxo de informações de resumo](summary-information-stream.md) (parcial)



| Propriedade       | Valor                                  |
|----------------|----------------------------------------|
| PID \_ REVNUMBER | {000C1101-0000-0000-C000-00000000047} |



 

[Tabela de propriedades](property-table.md) (parcial)



| Propriedade                           | Valor                                  |
|------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md) | {80F7E030-A751-11D2-A7D4-006097C99860} |
| [**Upgradecode**](upgradecode.md) | {8FC70000-88A0-4b41-82B8-8905D4AAA904C} |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Códigos de pacote](package-codes.md)
</dt> <dt>

[Códigos de produto](product-codes.md)
</dt> <dt>

[**Propriedade Resumo do Número de Revisão**](revision-number-summary.md)
</dt> <dt>

[**Propriedade UpgradeCode**](upgradecode.md)
</dt> <dt>

[**Propriedade ProductCode**](productcode.md)
</dt> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



