---
description: O Proteção de Recursos do Windows (WRP) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais instalados como parte do Windows Vista ou do Windows Server 2008.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Detectando substituição de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1855b98ca5834ef9e13e2f48bf7cca492e94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662992"
---
# <a name="detecting-resource-replacement"></a>Detectando substituição de recursos

O Proteção de Recursos do Windows (WRP) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais instalados como parte do Windows Vista ou do Windows Server 2008.

A WRP protege arquivos, pastas e chaves do registro no Windows Vista ou no Windows Server 2008, detectando e impedindo tentativas de substituição de recursos protegidos. Essa proteção baseia-se em uma DACL (lista de controle de acesso discricional) do Windows e ACLs (listas de controle de acesso) definidas para recursos protegidos. Permissão para acesso completo para modificar recursos protegidos por WRP é restrita a TrustedInstaller. Os recursos protegidos por WRP só podem ser alterados usando os [mecanismos de substituição de recursos com suporte](supported-file-replacement-mechanisms.md) com o serviço instalador de módulos do Windows. Os aplicativos que tentam modificar um recurso protegido por WRP nunca alteram o recurso e podem receber uma mensagem de erro que indica que o acesso ao recurso foi negado.

Os aplicativos e instaladores podem usar as funções [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) e [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) para determinar se um arquivo ou chave do registro está protegido.

* * Windows Server 2003 e Windows XP: * *

A WFP (proteção de arquivo do Windows) protege os arquivos do sistema detectando tentativas de substituição de arquivos protegidos do sistema. Essa proteção é disparada depois que a WFP recebe uma notificação de alteração de diretório para um arquivo em um diretório protegido. Quando a WFP recebe essa notificação, ela determina qual arquivo foi alterado. Se o arquivo estiver protegido, a WFP pesquisará a assinatura do arquivo em um arquivo de catálogo para determinar se o novo arquivo é a versão correta. Se a versão do arquivo não estiver correta, o sistema substituirá o arquivo pela versão correta da mídia de cache ou de distribuição, dependendo se o arquivo está localizado no cache. A WFP procura o arquivo correto na seguinte ordem:

1.  Pesquise o diretório de cache.
2.  Pesquise o caminho de instalação de rede, se o sistema tiver sido instalado usando a instalação de rede.
3.  Pesquise em um CD-ROM do Windows, se o sistema tiver sido instalado do CD-ROM.

Se a WFP não conseguir localizar automaticamente o arquivo nos dois primeiros locais, ele exibirá a seguinte mensagem:

![mensagem WFP exibida quando o arquivo não foi encontrado no diretório de cache ou no caminho de instalação de rede](images/wfp-1.png)

Se o sistema tiver sido instalado usando um CD-ROM, a WFP exibirá a seguinte mensagem:

![mensagem WFP exibida para solicitar que o usuário insira o CD-ROM do Windows](images/wfp-2.png)

Se um administrador não estiver conectado, a WFP não poderá exibir nenhuma dessas caixas de diálogo. A WFP exibirá a caixa de diálogo depois que um administrador fizer logon.

A WFP também registra a tentativa de substituição de arquivo no log de eventos do sistema. Se o administrador cancelou a restauração do arquivo correto, a WFP registra o cancelamento.

## <a name="retrieving-the-list-of-protected-files"></a>Recuperando a lista de arquivos protegidos

O exemplo a seguir mostra como os aplicativos e instaladores podem usar a função [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) para obter a lista completa de arquivos protegidos.


```C++
#include <windows.h>
#include <sfc.h>
#include <stdio.h>

#pragma comment(lib, "sfc")

void wmain (int argc, WCHAR ** argv)
{  UNREFERENCED_PARAMETER(argc);    
   PROTECTED_FILE_DATA pfd = {0};
   BOOL fResult;

   wprintf (L"List of protected files:\n\n", argv[1]);

   while (FALSE != (fResult = SfcGetNextProtectedFile (NULL, &pfd)))
   {
      wprintf (L"   %lu   %s\n", pfd.FileNumber, pfd.FileName);
   }

   if (GetLastError() == ERROR_NO_MORE_FILES)
   {
      wprintf (L"\nAll %lu protected files listed\n", pfd.FileNumber);
   }
   else
   {
      wprintf (L"\nerror %lu: SfcGetNextProtectedFile() failed unexpectedly\n", GetLastError());
   }

}
```



 

 



