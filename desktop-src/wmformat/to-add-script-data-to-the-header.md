---
title: Para adicionar dados de script ao cabeçalho
description: Para adicionar dados de script ao cabeçalho
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- SDK do Windows Media Format, adicionando dados de script aos cabeçalhos
- ASF (Advanced Systems Format), adicionando dados de script aos cabeçalhos
- ASF (formato de sistemas avançados), adicionando dados de script aos cabeçalhos
- scripts, adicionando dados aos cabeçalhos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105786153"
---
# <a name="to-add-script-data-to-the-header"></a>Para adicionar dados de script ao cabeçalho

Você pode incluir comandos de script no cabeçalho de um arquivo ASF. Para gravar comandos de script no cabeçalho no momento da codificação, execute as etapas a seguir. Execute estas etapas antes de chamar [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

1.  Obtenha um ponteiro para a interface **IWMHeaderInfo** chamando **IWMWriter:: QueryInterface**.
2.  Adicione cada comando de script desejado chamando [**IWMHeaderInfo:: addScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript). Cada chamada usa as duas cadeias de caracteres separadamente e o tempo de apresentação a ser usado para o comando como parâmetros.

Quando um aplicativo lê o arquivo, ele precisa recuperar todos os comandos de script. Para localizar todos os comandos de script no cabeçalho de um arquivo, execute as etapas a seguir. Isso deve ser feito antes de iniciar a reprodução.

1.  Obtenha um ponteiro para a interface **IWMHeaderInfo** do objeto leitor (ou objeto leitor síncrono) chamando o método **QueryInterface** de outra interface no objeto.
2.  Obtenha o número total de scripts no cabeçalho chamando [**IWMHeaderInfo:: GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).
3.  Execute um loop por todos os scripts no cabeçalho, um de cada vez, usando chamadas para [**IWMHeaderInfo:: GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).
4.  Crie uma lista das horas de apresentação para que seu aplicativo possa reagir aos comandos no momento apropriado.

> [!Note]  
> Ao usar o DRM para criptografar um arquivo, nenhum comando de script pode ter um horário de apresentação de 0.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Usando comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




