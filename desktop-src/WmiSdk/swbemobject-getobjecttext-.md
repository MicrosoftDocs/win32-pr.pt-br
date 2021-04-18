---
description: O \_ método GetObjectText do objeto SWbemObject retorna uma renderização textual do objeto.
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: Método de SWbemObject.GetObjectText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2447d8361d02626e1f5ea8fae1928ffd563d52ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749469"
---
# <a name="swbemobjectgetobjecttext_-method"></a>Método SWbemObject. GetObjectText \_

O **método \_ GetObjectText** do objeto [**SWbemObject**](swbemobject.md) retorna uma renderização textual do objeto. Esse objeto pode ser usado para exibir o conteúdo de um objeto. Atualmente, há suporte apenas para a sintaxe do MOF como um formato de saída. Observe que o texto MOF retornado não contém todas as informações sobre o objeto; o texto MOF contém apenas informações suficientes para que o compilador MOF possa recriar o objeto original. Por exemplo, não há informações sobre os qualificadores propagados ou as propriedades da classe pai.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado e deve ser 0 (zero) se especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, esse método retornará uma cadeia de caracteres que contém o texto de saída.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **GetObjectText \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Foi especificado um parâmetro inválido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="examples"></a>Exemplos

O código a seguir, extraído da [lista a definição de uma classe WMI no formato MOF](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) de exemplo de código VBScript na galeria do TechNet, recupera e exibe a representação textual de uma definição de classe WMI na sintaxe MOF (formato MOF).


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



 

 




