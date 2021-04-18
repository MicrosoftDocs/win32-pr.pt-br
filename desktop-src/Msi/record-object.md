---
description: O objeto Record é um contêiner para manter e transferir um número variável de valores.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Objeto de registro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751634"
---
# <a name="record-object"></a>Objeto de registro

O objeto **Record** é um contêiner para manter e transferir um número variável de valores. Os campos dentro do registro são indexados numericamente e podem conter cadeias de caracteres, inteiros, objetos e valores nulos. Os campos além do tamanho do registro alocado são tratados como tendo valores nulos permanentemente. O campo número 0 está reservado.

## <a name="members"></a>Membros

O objeto **Record** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Record** tem esses métodos.



| Método                                  | Descrição                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**ClearData**](record-cleardata.md)   | Limpa os dados em todos os campos, definindo-os como NULL.<br/>                                      |
| [**FormatText**](record-formattext.md) | Formata os campos de acordo com o modelo no campo 0.<br/>                                      |
| [**ReadStream**](record-readstream.md) | Lê um número especificado de bytes de um campo de registro que contém dados de fluxo.<br/>                |
| [**SetStream**](record-setstream.md)   | Copia o conteúdo do arquivo especificado para o campo registro designado como dados de fluxo.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **Record** tem essas propriedades.



| Propriedade                                             | Tipo de acesso           | Descrição                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**DataSize**](record-datasize.md)<br/>       |                       | Retorna o tamanho dos dados para o campo designado.<br/>                             |
| [**FieldCount**](record-fieldcount.md)<br/>   |                       | Obtém o número de campos no registro.<br/>                                        |
| [**IntegerData**](record-integerdata.md)<br/> | Leitura/gravação<br/> | Transfere dados inteiros de 32 bits para ou para fora de um campo especificado dentro do registro.<br/> |
| [**Énulo**](record-isnull.md)<br/>           |                       | Retornará true se o campo indicado for nulo e false se o campo contiver dados.<br/>  |
| [**StringData**](record-stringdata.md)<br/>   | Leitura/gravação<br/> | Transfere dados de cadeia de caracteres para ou para fora de um campo especificado dentro do registro.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método CreateRecord**](installer-createrecord.md)
</dt> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




