---
title: Compilação offline
description: A ferramenta de compilador de efeito (fxc.exe) foi projetada para compilação offline de sombreadores HLSL.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- FXC, compilação offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a15d3a71dbfb79541a75bd38cb28140d832b45e75a88a52b2d0c8988865f12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406326"
---
# <a name="offline-compiling"></a>Compilação offline

A ferramenta de compilador de efeito (fxc.exe) foi projetada para compilação offline de sombreadores HLSL.

## <a name="compiling-with-the-current-compiler"></a>Compilando com o compilador atual

Os modelos de sombreador com suporte do compilador atual são mostrados em [perfis](dx-graphics-tools-fxc-syntax.md). Este exemplo compila um sombreador de pixel para o destino do modelo do sombreador 5,1.

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

Neste exemplo:

-   \_o PS 5 \_ 1 é o perfil de destino.
-   PixelShader1. fxc é o arquivo de objeto de saída que contém o sombreador compilado.
-   PixelShader1. HLSL é a origem.

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

As opções de depuração incluem opções adicionais para desabilitar a OD (otimizações de compilador) e habilitar informações de depuração (Zi), como números de linha e símbolos.

Para obter uma lista completa das opções de linha de comando, consulte a página [sintaxe](dx-graphics-tools-fxc-syntax.md) .

## <a name="compiling-with-the-legacy-compiler"></a>Compilando com o compilador herdado

A partir do Direct3D 10, não há mais suporte para alguns modelos de sombreador. Isso inclui modelos de sombreador de pixel: PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 e PS \_ 1 \_ 4 que dão suporte a recursos muito limitados e dependem de hardware. O compilador foi reprojetado com o modelo de sombreador 2 (ou superior), o que permite maior eficiência com a compilação. Isso, é claro, exigirá que você esteja executando o hardware que dá suporte a modelos de sombreamento 2 e superior.

Observe também que você deve consultar as notas de versão do SDK associadas à sua versão do compilador FXC para o comportamento afetado pela opção/GEC.

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a>Usando a ferramenta de compilador de efeito em um subprocesso

Se fxc.exe for gerado como um subprocesso por um aplicativo, é importante garantir que o aplicativo Verifique e leia os dados na saída ou os pipes de erro passados para a função CreateProcess. Se o aplicativo só aguardar a conclusão do subprocesso e um dos pipes ficar cheio, o subprocesso nunca será concluído.

O código de exemplo a seguir ilustra a espera em um subprocesso e a leitura dos pipes de erro e saída anexados ao subprocesso. O conteúdo da `WaitHandles` matriz corresponde a identificadores para o subprocesso, o pipe para stdout e o pipe para stderr.

```cpp
HANDLE WaitHandles[] = {
  piProcInfo.hProcess, hReadOutPipe, hReadErrorPipe
};

const DWORD BUFSIZE = 4096;
BYTE buff[BUFSIZE];

while (1)
{
    DWORD dwBytesRead, dwBytesAvailable;

    dwWaitResult = WaitForMultipleObjects(3, WaitHandles, FALSE, 60000L);

    // Read from the pipes...
    while (PeekNamedPipe(hReadOutPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadOutPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamOut << std::string((char*)buff, (size_t)dwBytesRead);
    }
    while (PeekNamedPipe(hReadErrorPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadErrorPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamError << std::string((char*)buff, (size_t)dwBytesRead);
    }

    // Process is done, or we timed out:
    if (dwWaitResult == WAIT_OBJECT_0 || dwWaitResult == WAIT_TIMEOUT)
        break;
}
```

Para obter informações adicionais sobre como gerar um processo, consulte a página de referência de [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).

## <a name="related-topics"></a>Tópicos relacionados

* [Efeito-ferramenta do compilador](fxc.md)