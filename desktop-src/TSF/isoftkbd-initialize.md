---
title: Método de inicialização de ISoftKbd (Softkbdc. h)
description: O método de inicialização ISoftKbd inicializa todos os campos necessários para um teclado virtual e gera layouts de teclado flexível padrão.
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Inicializar o método de estrutura de serviços de texto
- Inicializar o método Text Services Framework, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método Initialize
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644326"
---
# <a name="isoftkbdinitialize-method"></a>Método ISoftKbd:: Initialize

O método **ISoftKbd:: Initialize** inicializa todos os campos necessários para um teclado virtual e gera layouts de teclado flexível padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Initialize();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                | Descrição                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





