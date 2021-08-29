---
description: a função UiCreatePatchPackageEx usa um arquivo de criação de pacote (arquivo. pcp) e gera um pacote de patches Windows Installer (pacote. msp). Chamar Msimsp.exe é o método recomendado para usar Patchwiz.dll.
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: UiCreatePatchPackageEx (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9c610aa6b03990eb4bb9fb34ce84568c9164a88ff2455b9c649436b3d327c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039388"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a>UiCreatePatchPackageEx (Patchwiz.dll)

a função UiCreatePatchPackageEx usa um arquivo de criação de pacote (arquivo. pcp) e gera um pacote de patches Windows Installer (pacote. msp). Chamar [Msimsp.exe](msimsp-exe.md) é o método recomendado para usar [Patchwiz.dll](patchwiz-dll.md).

A função UiCreatePatchPackageEx está disponível começando com Patchwiz.dll versão 4,0 e estende a funcionalidade da função [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*
</dt> <dd>

Caminho completo do arquivo de propriedades de criação de patch (arquivo. PCP) para este patch.

</dd> <dt>

<span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*
</dt> <dd>

caminho completo do pacote de patches Windows Installer (arquivo. msp) a ser criado. Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido. Se for **nulo** ou uma cadeia de caracteres vazia, a função usará o valor de PatchOutputPath na [tabela de Propriedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md).

</dd> <dt>

<span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*
</dt> <dd>

Caminho completo de um arquivo de log de texto que será anexado. Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido.

</dd> <dt>

<span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*
</dt> <dd>

Identificador para uma janela que exibe o texto de status. Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido.

</dd> <dt>

<span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*
</dt> <dd>

Local para arquivos temporários. Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido. O usuário deve ter privilégios suficientes para ler e gravar nessa pasta. O local padrão é% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

Se **for true**, remova a pasta temporária e todo o seu conteúdo, se presente. Se **false** e a pasta estiver presente, a função falhará.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

Esse parâmetro pode ser definido como um ou uma combinação dos valores a seguir para especificar opções de log ou de interface do usuário.



| Sinalizador            | Valor       | Significado                                  |
|-----------------|-------------|------------------------------------------|
| LOGNONE         | 0x00000000  | Não grave nenhuma mensagem no log.            |
| LOGINFO         | 0x00000001  | Grave mensagens informativas no log. |
| LOGWARN         | 0x00000002  | Grave avisos no log.               |
| LOGERR          | 0x00000004  | Grave mensagens de erro no log.         |
| LOGPERFMESSAGES | 0x00000008  | Grave mensagens de desempenho no log.   |
| UINONE          | 0x00000000f | Não exibir a interface do usuário.       |
| UIALL           | 0x00000010  | Exibir a interface do usuário.              |



 

</dd> <dt>

<span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*
</dt> <dd>

Reservado. Esse parâmetro deve ser definido como zero.

</dd> </dl>

## <a name="return-values"></a>Valores de retorno

Consulte a tabela em [valores de retorno para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Comentários

para obter um exemplo de como criar um arquivo. pcp e usar o [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) para gerar um pacote de patches Windows Installer, consulte a seção [um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md).

A criação de um patch requer uma imagem de instalação descompactada, como uma imagem administrativa ou uma imagem de instalação descompactada de um CD-ROM. [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) não gera patches binários para arquivos em gabinetes.

 

 



