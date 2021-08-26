---
title: Converter autoconverteto
description: Especifica a conversão automática de uma determinada classe de objetos em uma nova classe de objetos.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- Conversão de chave de registro COM autoconverterto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ea2b32445bb7107dcbfdc2aec8aee518fdd474674e76fdbd820265d06b6160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097046"
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

 

 




