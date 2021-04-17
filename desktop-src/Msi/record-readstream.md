---
description: O método ReadStream do objeto de registro lê um número especificado de bytes de um campo de registro que contém dados de fluxo.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Método record. ReadStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758950"
---
# <a name="recordreadstream-method"></a>Método record. ReadStream

O método **ReadStream** do objeto de [**registro**](record-object.md) lê um número especificado de bytes de um campo de registro que contém dados de fluxo.

## <a name="syntax"></a>Sintaxe


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*campo* 
</dt> <dd>

O número de campo necessário do valor dentro do registro, baseado em 1.

</dd> <dt>

*length* 
</dt> <dd>

O número necessário de bytes para ler a partir do fluxo.

</dd> <dt>

*format* 
</dt> <dd>

Interpretação necessária e retorno dos bytes de dados.



| Nome do parâmetro                                                                                                                                                                                                                                                                  | Significado                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <dt>**msiReadStreamInteger**</dt> <dt>0</dt> </dl> | Como um inteiro longo, o comprimento deve ser de 1 a 4.<br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <dt>**msiReadStreamBytes**</dt> <dt>1</dt> </dl>         | Os dados como um **BSTR**– um byte por caractere.<br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <dt>**msiReadStreamAnsi**</dt> <dt>2</dt> </dl>             | Os bytes ANSI convertidos em um **BSTR** Unicode.<br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <dt>**msiReadStreamDirect**</dt> <dt>3</dt> </dl>     | Os pares de bytes retornados diretamente como um **BSTR**.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma cadeia de caracteres que contém o número solicitado de bytes lidos de um campo de registro.

## <a name="remarks"></a>Comentários

O valor retornado de um campo inexistente é um valor vazio. Se o fluxo tiver menos bytes que a contagem solicitada, a cadeia de caracteres retornada será reduzida adequadamente.

Para obter um exemplo desse método, consulte [Copiar arquivo ANSI em um campo de banco de dados](copy-ansi-file-into-a-database-field.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




