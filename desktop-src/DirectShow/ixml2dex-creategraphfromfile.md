---
description: Método IXml2Dex::CreateGraphFromFile – Não implementado.
ms.assetid: b476e0c9-1432-4644-8002-154797a2a594
title: Método IXml2Dex::CreateGraphFromFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.CreateGraphFromFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e3ce23fd92a843219490202d42ead4e386deddc8c056b883d2ac45b77a8555d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817063"
---
# <a name="ixml2dexcreategraphfromfile-method"></a>Método IXml2Dex::CreateGraphFromFile

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Não implementado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateGraphFromFile(
   IUnknown **ppGraph,
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppGraph* 
</dt> <dd>

Reservado.

</dd> <dt>

*pTimeline* 
</dt> <dd>

Reservado.

</dd> <dt>

*FileName* 
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IXml2Dex Interface**](ixml2dex.md)
</dt> </dl>

 

 



