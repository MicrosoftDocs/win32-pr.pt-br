---
description: ICE80 valida que o valor da propriedade de resumo do modelo ( \_ modelo PID) especifica corretamente &\# 0034; Intel64&\# 0034;, &\# 0034; x64&\# 0034; ou &\# 0034; Intel&\# 0034; dependendo da presença de componentes de 64 bits ou scripts de ação personalizados.
ms.assetid: fd2a15cf-d117-4a87-a26e-caff4b12a2e9
title: ICE80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7be298e406db40b76a54eadbe12e99175e0058d97c4d57c5a4b1cd842b000f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339936"
---
# <a name="ice80"></a>ICE80

ICE80 valida que o valor da propriedade de [**Resumo do modelo**](template-summary.md) ( \_ modelo PID) especifica corretamente "Intel64", "x64", "Arm64" ou "Intel", dependendo da presença de componentes de 64 bits ou scripts de ação personalizados. ICE80 verifica a [tabela](component-table.md) de componentes em busca de qualquer componente com o atributo **msidbComponentAttributes64bit** e verifica a [tabela CustomAction](customaction-table.md) para todos os scripts com o atributo **msidbCustomActionType64BitScript** . ICE80 verifica se um pacote com "Intel64", "x64" ou "Arm64" em sua propriedade de **Resumo do modelo** também tem uma propriedade de [**Resumo de contagem de página**](page-count-summary.md) (PID \_ PAGECOUNT) de pelo menos 150.

ICE80 também valida que a ID de idioma especificada pela propriedade [**ProductLanguage**](productlanguage.md) deve estar contida na propriedade [**Summary do modelo**](template-summary.md) .

para obter mais informações, consulte [Windows Installer em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md).

## <a name="result"></a>Resultado

ICE80 posta os erros a seguir.



| Erro                                                                                                                                                                   | Descrição                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Este pacote contém o componente de 64 bits ' \[ 1 \] ', mas a propriedade de [**Resumo do modelo**](template-summary.md) não contém Intel64, x64 ou Arm64.                    | A [tabela de componentes](component-table.md)contém um componente com o atributo **msidbComponentAttributes64bit** e a propriedade [**Summary do modelo**](template-summary.md) não contém Intel64, x64 ou Arm64.        |
| Este pacote contém o script de ação personalizada de 64 bits ' \[ 1 \] ', mas a propriedade de [**Resumo do modelo**](template-summary.md) não contém Intel64, x64 ou Arm64.         | A [tabela CustomAction](customaction-table.md) contém uma ação personalizada de script com o **msidbCustomActionType64BitScript** , mas a propriedade de [**Resumo do modelo**](template-summary.md) não contém Intel64, x64 ou Arm64. |
| Valor inadequado no fluxo de informações de resumo para% s.                                                                                                                         | Retornado para a \_ Propriedade do modelo PID se essa propriedade for uma cadeia de caracteres vazia ou não um tipo de um ' VT \_ LPSTR '. Retornado para PID \_ PageCount se essa propriedade não for um tipo de \_ i4 VT.<br/>                                         |
| Este pacote está marcado com Intel64, mas tem um esquema menor que 150.                                                                                                  | A \_ propriedade de modelo PID do pacote é Intel64, mas sua \_ Propriedade PID PageCount é menor que 150.                                                                                                            |
| Este pacote é marcado com x64, mas tem um esquema inferior a 200.                                                                                                      | A \_ propriedade de modelo PID do pacote é x64, mas sua \_ Propriedade PID PageCount é menor que 200.                                                                                                            |
| Este pacote está marcado com Arm64, mas tem um esquema menor que 500.                                                                                                    | A \_ propriedade de modelo PID do pacote é Arm64, mas sua \_ Propriedade PID PageCount é menor que 500.                                                                                                            |
| Este pacote de 32 bits está usando a propriedade de bit 1 de 64 \[\]                                                                                                                       | Um pacote de 32 bits está usando uma propriedade de 64 bits.                                                                                                                                                                              |
| Este pacote de 32 bits está usando o tipo de localizador de bit 64 na entrada da tabela RegLocator \[ 1\]                                                                                         | Um pacote de 32 bits contém **msidbLocatorType64bit** no campo tipo da [tabela RegLocator](reglocator-table.md).                                                                                                    |
| Este 64BitComponent \[ 1 \] usa o 32BitDirectory \[ 3\]                                                                                                                     | Um componente de 64 bits está usando um diretório de 32 bits.                                                                                                                                                                           |
| Este 32BitComponent \[ 1 \] usa o 64BitDirectory \[ 3\]                                                                                                                     | Um componente de 32 bits está usando um diretório de 64 bits.                                                                                                                                                                           |
| A propriedade '[**ProductLanguage**](productlanguage.md)' na tabela de propriedades tem um valor de ' \[ 2 \] ', que não está contido no fluxo da propriedade de resumo do modelo. | O valor da propriedade [**ProductLanguage**](productlanguage.md) não está listado na propriedade [**Summary do modelo**](template-summary.md) .                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> <dt>

[Windows Instalador em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md)
</dt> </dl>

 

 




