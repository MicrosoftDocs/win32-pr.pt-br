---
title: Propriedade ResourceLocator. ResourceURI (WSManDisp. h)
description: Obtém ou define o URI do recurso em um objeto ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows da propriedade resourceuri
- propriedade resourceuri Gerenciamento Remoto do Windows, objeto ResourceLocator
- objeto ResourceLocator Gerenciamento Remoto do Windows, propriedade resourceuri
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323240462dad32ba757897798b663b78b373ebb3ab3e60c3387dd7da8eef4c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642856"
---
# <a name="resourcelocatorresourceuri-property"></a>Propriedade ResourceLocator. ResourceURI

Obtém ou define o [*URI do recurso*](windows-remote-management-glossary.md) em um objeto [**ResourceLocator**](resourcelocator.md) . Você pode fornecer um objeto [**ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres que identifica o recurso. Ao definir o URI de recurso para um objeto [**ResourceLocator**](resourcelocator.md) , o URI deve conter apenas o caminho.

## <a name="remarks"></a>Comentários

Veja a seguir um exemplo de um caminho apropriado para [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

O caminho a seguir não funciona porque ele contém uma chave para uma instância específica. Use o método [**ResourceLocator. Addseletor**](resourcelocator-addselector.md) para especificar uma instância específica.

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

**IWSManResourceLocator:: ResourceURI** é o método C++ correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





