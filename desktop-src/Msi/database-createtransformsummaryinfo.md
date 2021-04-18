---
description: O método CreateTransformSummaryInfo do objeto Database cria e popula o fluxo de informações resumidas de um arquivo de transformação existente. Esse método preenche as propriedades com o ProductCode base e de referência e ProductVersion.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Método Database. CreateTransformSummaryInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 824f46fd17eb51fddbf09c2f34569574c50c570a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780960"
---
# <a name="databasecreatetransformsummaryinfo-method"></a>Método Database. CreateTransformSummaryInfo

O método **CreateTransformSummaryInfo** do objeto [**Database**](database-object.md) cria e popula o fluxo de informações resumidas de um arquivo de transformação existente. Esse método preenche as propriedades com o [**ProductCode**](productcode.md) base e de referência e [**ProductVersion**](productversion.md).

## <a name="syntax"></a>Sintaxe


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*reference* 
</dt> <dd>

Banco de dados necessário que não inclui as alterações.

</dd> <dt>

*storage* 
</dt> <dd>

O nome do arquivo de transformação gerado. Isso é opcional.

</dd> <dt>

*errorConditions* 
</dt> <dd>

Condições de erro necessárias que devem ser suprimidas quando a transformação é aplicada. Combine um ou mais dos seguintes valores de condição de erro.



| Nome da condição de erro                                                                                                                                                                                                                                                                                                                                        | Significado                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <dt>**msiTransformErrorNone**</dt> <dt>0</dt> </dl>                                                                         | Nenhuma das condições a seguir.<br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt> </dl>                                 | Adiciona uma linha que já existe.<br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt> </dl>         | Exclui uma linha que não existe.<br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt> </dl>                         | Adiciona uma tabela que já existe.<br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt> </dl> | Exclui uma tabela que não existe.<br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt> </dl>        | Atualiza uma linha que não existe.<br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt> </dl>                                | As páginas de código de transformação e de banco de dados não coincidem e nenhuma página de código é neutra.<br/> |



 

</dd> <dt>

*validation* 
</dt> <dd>

Necessário quando a transformação é aplicada a um banco de dados; mostra quais propriedades devem ser validadas para verificar se essa transformação pode ser aplicada ao banco de dados. As propriedades estão todas contidas no [conjunto de propriedades fluxo de informações de resumo](summary-information-stream-property-set.md).

Combine um ou mais dos valores a seguir.



| Sinalizador de validação                                                                                                                                                                                                                                                                                                         | Significado                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <dt>**msiTransformValidationNone**</dt> <dt>0</dt> </dl>                 | Nenhuma validação feita.<br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <dt>**msiTransformValidationLanguage**</dt> <dt>1</dt> </dl> | O idioma padrão deve corresponder ao banco de dados base.<br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <dt>**msiTransformValidationProduct**</dt> <dt>2</dt> </dl>     | O produto deve corresponder ao banco de dados base.<br/>          |



 

Para validar a versão do produto, primeiro escolha um ou mais desses três sinalizadores para indicar a quantidade de verificação da versão.



| Sinalizador de validação                                                                                                                                                                                                                                                                                                              | Significado                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt> </dl>      | Verifica somente a versão principal.<br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt> </dl>     | Verifica apenas a versão principal e secundária.<br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt> </dl> | Verifica as versões principal, secundária e de atualização.<br/> |



 

Em seguida, escolha uma das opções a seguir para indicar a relação necessária entre a versão do produto do banco de dados à qual a transformação está sendo aplicada e a do banco de dados base.



| Sinalizador de validação                                                                                                                                                                                                                                                                                                                                   | Significado                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <dt>**msiTransformValidationLess**</dt> <dt>64</dt> </dl>                                          | Versão aplicada < versão base<br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt> </dl>             | Versão aplicada <= versão base<br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <dt>**msiTransformValidationEqual**</dt> <dt>256</dt> </dl>                                     | Versão aplicada = versão base<br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt> </dl> | Versão aplicada >= versão base<br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <dt>**msiTransformValidationGreater**</dt> <dt>1024</dt> </dl>                            | Versão aplicada > versão base<br/>  |



 

Para validar que a transformação está sendo aplicada a um pacote com o [**UpgradeCode**](upgradecode.md)apropriado, defina o sinalizador a seguir.



| Sinalizador de validação                                                                                                                                                                                                                                                                                                                        | Significado                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt> </dl> | Valida que a transformação é o [**UpgradeCode**](upgradecode.md)apropriado.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para criar um fluxo de informações de resumo para uma transformação, as propriedades [**ProductCode**](productcode.md) e [**ProductVersion**](productversion.md) devem ser definidas nas tabelas de [Propriedades](property-table.md) dos bancos de dados base e de referência. Se msiTransformValidationUpgradeCode for usado, a propriedade [**UpgradeCode**](upgradecode.md) deverá ser definida em ambos os bancos de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Transformações de banco de dados](database-transforms.md)
</dt> </dl>

 

 




