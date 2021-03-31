---
title: Converter autoconverteto
description: Especifica a conversão automática de uma determinada classe de objetos em uma nova classe de objetos.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- Conversão de chave de registro COM autoconverterto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822152"
---
# <a name="autoconvertto"></a>Converter autoconverteto

Especifica a conversão automática de uma determinada classe de objetos em uma nova classe de objetos.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz de reg** que especifica o identificador de classe do objeto para o qual o objeto ou a classe de objetos fornecida deve ser convertida.

Normalmente, essa chave é usada para converter automaticamente os arquivos criados por uma versão mais antiga de um aplicativo em uma versão mais recente do aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**OleDoAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**OleGetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**OleSetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




