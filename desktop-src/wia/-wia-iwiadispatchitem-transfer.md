---
description: O método de transferência do objeto item transfere dados de um dispositivo para um arquivo. Esse método aplica-se somente a itens de tipo de dispositivo.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Método item. Transfer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783767"
---
# <a name="itemtransfer-method"></a>Método item. Transfer

O método de **transferência** do objeto [**Item**](-wia-item.md) transfere dados de um dispositivo para um arquivo. Esse método aplica-se somente a itens de tipo de dispositivo.

## <a name="syntax"></a>Sintaxe


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do arquivo* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome do arquivo para o qual os dados são transferidos.

</dd> <dt>

*AsyncTransfer* \[ no\]
</dt> <dd>

Tipo: **\_ booliano de variante**

Um valor booliano que especifica se a transferência deve ser executada como uma chamada assíncrona.

<dt>



 (Variante \_ BOOL


</dt> <dd>

Padrão. Defina esse valor como **true** se a chamada deve ser assíncrona (consulte **comentários**).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método aplica-se somente a itens de tipo de arquivo. O método verifica se o item dá suporte a esse método antes de tentar concluir a transferência de dados.

Use "Clipboard" como o parâmetro *filename* para transferir um item para a área de transferência.

Defina o valor de *AsyncTransfer* como **false** para transferências em qualquer aplicativo ou script executado em um ambiente que termine um processo no final de um script, como o WSH (Windows Script Host). Caso contrário, o script pode terminar e o processo é encerrado antes de a transferência ser concluída.

O método de **transferência** não tem nenhum valor de retorno. Após a conclusão de uma transferência, esse método envia um evento [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) para o script ou aplicativo.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o uso do método de **transferência** para transferir dados de um dispositivo.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |



 

 




