---
title: Apagando um CD regravável
description: Apagando um CD regravável
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, apagando CDs regraváveis
- gravando CDs, apagando CDs regraváveis
- apagando CDs regraváveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007112"
---
# <a name="erasing-a-rewritable-cd"></a>Apagando um CD regravável

A interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) fornece um método para apagar discos CD-RW. Antes de apagar um CD, você deve primeiro verificar se a operação tem suporte. Para obter mais informações, consulte [recuperando a unidade e o status do disco](retrieving-the-drive-and-disc-status.md).

Para começar a apagar o conteúdo de um CD regravável, chame [IWMPCdromBurn:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando um CD**](burning-a-cd.md)
</dt> <dt>

[**Recuperar a interface de gravação de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Iniciando o processo de gravação**](starting-the-burn-process.md)
</dt> <dt>

[**Recuperando a unidade e o status do disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recuperando o status da gravação**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




