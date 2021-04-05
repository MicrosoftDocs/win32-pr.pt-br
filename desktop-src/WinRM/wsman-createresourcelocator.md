---
title: Método WSMan. CreateResourceLocator (WSManDisp. h)
description: Cria um objeto ResourceLocator que pode ser usado em vez de especificar um URI de recurso em operações de objeto de sessão, como Session. Get, Session. Put ou Session. Enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método CreateResourceLocator
- Método CreateResourceLocator Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método CreateResourceLocator
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918362"
---
# <a name="wsmancreateresourcelocator-method"></a>Método WSMan. CreateResourceLocator

Cria um objeto [**ResourceLocator**](resourcelocator.md) que pode ser usado em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintaxe


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*URI* \[ do em, opcional\]
</dt> <dd>

O URI de recurso para o recurso. Para obter mais informações sobre cadeias de caracteres de URI, consulte [URIs de recurso](resource-uris.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um objeto [**ResourceLocator**](resourcelocator.md) que pode ser usado para executar operações WinRM locais ou remotas.

## <a name="remarks"></a>Comentários

Se a propriedade **FragmentDialect** não for especificada no objeto [**ResourceLocator**](resourcelocator.md) , o padrão será a especificação XPath 1,0. Para obter mais informações, confira [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir cria um objeto [**ResourceLocator**](resourcelocator.md) e Obtém o valor da propriedade de **Descrição** do adaptador de rede da instância do [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) com um índice de "1".


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**Session**](session.md)
</dt> </dl>

 

