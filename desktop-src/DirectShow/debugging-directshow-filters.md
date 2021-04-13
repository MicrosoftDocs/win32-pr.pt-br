---
description: Muitos dos recursos de depuração descritos neste tópico são implementados na biblioteca de classes base do DirectShow. Para obter mais informações, consulte classes base do DirectShow.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Depuração de filtros do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500676"
---
# <a name="debugging-directshow-filters"></a>Depuração de filtros do DirectShow

Muitos dos recursos de depuração descritos neste tópico são implementados na biblioteca de classes base do DirectShow. Para obter mais informações, consulte [classes base do DirectShow](directshow-base-classes.md).

## <a name="assertion-checking"></a>Verificação de asserção

Use a verificação de asserção livremente. As asserções podem verificar suposições que você faz em seu código sobre pré-condições e pré-condições. O DirectShow fornece várias macros de asserção. Para obter mais informações, consulte [declarações e macros de ponto de interrupção](assert-and-breakpoint-macros.md).

## <a name="object-names"></a>Nomes de objeto

Em compilações de depuração, há uma lista global de objetos que derivam da classe [**CBaseObject**](cbaseobject.md) . À medida que os objetos são criados, eles são adicionados à lista. Quando eles são destruídos, eles são removidos da lista. Para exibir uma lista desses objetos, chame a função [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) .

O método de construtor para a classe base [**CBaseObject**](cbaseobject.md) — e a maioria das classes derivadas dela — inclui um parâmetro para o nome do objeto. Dê aos seus objetos nomes exclusivos para identificá-los. Use a macro [**Name**](name.md) quando você declarar o nome, de modo que o nome seja alocado somente em builds de depuração. Em compilações de varejo, o nome se torna **nulo**.

## <a name="debug-logging"></a>Log de depuração

A função [**DbgLog**](dbglog.md) exibe mensagens de depuração à medida que seu programa é executado. Use essa função para rastrear a execução do seu aplicativo ou filtro. Você pode registrar códigos de retorno, os valores de variáveis e quaisquer outras informações relevantes.

Cada mensagem de depuração tem um tipo, como rastreamento de LOG \_ ou \_ erro de log, e um nível de depuração, que indica a importância da mensagem. As mensagens com níveis inferiores de depuração são mais importantes do que aquelas com níveis mais altos.

No exemplo a seguir, um filtro hipotético desconecta um PIN de uma matriz de Pins. Se a tentativa de desconexão for realizada com sucesso, o filtro exibirá uma mensagem de rastreamento de LOG \_ . Se a tentativa falhar, ela exibirá uma \_ mensagem de erro de log:


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



Ao depurar, você pode definir o nível de depuração para cada tipo de mensagem. Além disso, cada módulo (DLL ou executável) mantém seus próprios níveis de depuração. Se você estiver testando um filtro, gere os níveis de depuração para a DLL que contém o filtro.

Para obter mais informações, consulte [depurar funções de saída](debug-output-functions.md).

## <a name="critical-sections"></a>Seções críticas

Para facilitar o controle dos deadlocks, inclua as asserções que determinam se o código de chamada possui uma determinada seção crítica. As funções [**CritCheckIn**](critcheckin.md) e [**CritCheckOut**](critcheckout.md) indicam se o thread de chamada possui uma seção crítica. Normalmente, você chamaria essas funções de dentro de uma macro Assert.

Você também pode usar a função [**DbgLockTrace**](dbglocktrace.md) para rastrear quando seções críticas são mantidas ou liberadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Depuração no DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



