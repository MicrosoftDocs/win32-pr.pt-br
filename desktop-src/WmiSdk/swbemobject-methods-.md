---
description: A propriedade Methods do objeto SWbemObject retorna um objeto SWbemMethodSet que é uma coleção dos métodos para a classe ou instância \_ atual. Esta propriedade é somente para leitura.
ms.assetid: ef9abced-5126-4698-b01e-f3e9c871162f
ms.tgt_platform: multiple
title: SWbemObject.Methods_ propriedade (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Methods_
- ISWbemObject.Methods_
- ISWbemObject.get_Methods_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e0442798a7630de20ff062a631baa335c5f6ed960900d571ca1d0e9e9a067f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991976"
---
# <a name="swbemobjectmethods_-property"></a>Propriedade SWbemObject.Methods \_

A **propriedade \_ Methods** do objeto [**SWbemObject**](swbemobject.md) retorna um objeto [**SWbemMethodSet**](swbemmethodset.md) que é uma coleção dos métodos para a classe ou instância atual. Esta propriedade é somente para leitura.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemObject.Methods_ As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="examples"></a>Exemplos

O exemplo [de código a](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1)seguir, retirado da Galeria do TechNet, descreve como listar todos os métodos de uma classe.


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Methods" 
WScript.Echo "---------------------------" 
  
For Each objClassMethod In objClass.Methods_ 
    WScript.Echo objClassMethod.Name 
Next 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




