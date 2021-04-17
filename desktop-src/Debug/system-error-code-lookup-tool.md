---
description: Descreve como usar a ferramenta de pesquisa de erros da Microsoft para localizar explicações de texto de códigos de erro hexadecimais no Windows.
title: A ferramenta de pesquisa de erros da Microsoft
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812135"
---
# <a name="the-microsoft-error-lookup-tool"></a>A ferramenta de pesquisa de erros da Microsoft

A ferramenta pesquisa de erros da Microsoft exibe o texto da mensagem que está associado a um código de status hexadecimal (ou outro código). Esse texto é definido em vários arquivos de cabeçalho de código-fonte da Microsoft, como Winerror. h, Setupapi. h e assim por diante.

A ferramenta é assinada digitalmente pela Microsoft. A seguir estão as informações de SHA256 para o download do arquivo:  

|Algoritmo |Hash |
| --- | --- |
|SHA256 |88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A |

> [!NOTE]
> Os ambientes de negócios podem restringir quais arquivos podem ser executados e de onde. Antes de baixar e executar essa ferramenta, verifique os seguintes detalhes:
> - Você precisa ter permissão ou uma exceção de segurança para poder baixar ou executar a ferramenta?
> - Você pode armazenar e executar essa ferramenta em seu computador (por exemplo, na pasta documentos)? Ou você precisa armazenar e executar a ferramenta em um computador especializado, como um servidor de arquivos central?

## <a name="usage"></a>Uso

1. Baixe a ferramenta selecionando [este link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).
1. Se você não especificou um local na etapa 1, vá para a pasta de download e copie ou mova o arquivo baixado (Err_6.4.5.exe) para a pasta na qual você armazenará a ferramenta. Você não precisa expandir ou instalar o arquivo.
   > [!NOTE]
   > Se você copiar ou mover o arquivo para uma pasta que está listada na variável de ambiente **path** do seu sistema operacional, ela funcionará em qualquer prompt de comando.

1. Abra uma janela de Prompt de Comando. Se necessário, altere o diretório para o local da ferramenta de pesquisa de erros.
1. Execute o comando a seguir:
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > Neste comando, \<*error code*> representa o código hexadecimal que você deseja pesquisar.

## <a name="examples"></a>Exemplos

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a>Mais informações

Tenha em mente que essa é uma ferramenta "pontual". A ferramenta de pesquisa de erros da Microsoft decodifica a maioria dos códigos de erro da Microsoft a partir da data em que a ferramenta foi compilada. À medida que novas versões do Windows adicionam novos eventos e códigos de erro, talvez seja necessário baixar uma nova versão da ferramenta de pesquisa de erros. Verifique o centro de download da Microsoft para obter uma nova versão ou veja os [códigos de erro](system-error-codes.md).
