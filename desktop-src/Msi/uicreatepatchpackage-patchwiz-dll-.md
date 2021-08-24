---
description: a função UiCreatePatchPackage usa um arquivo de criação de pacote (arquivo. pcp) e gera um pacote de patches Windows Installer (pacote. msp).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: UiCreatePatchPackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2802eb92d9df42a683053198ab14bbe7894fa512c63f25e1cd4afe060ea74c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810496"
---
# <a name="uicreatepatchpackage-patchwizdll"></a>UiCreatePatchPackage (Patchwiz.dll)

a função UiCreatePatchPackage usa um arquivo de criação de pacote (arquivo. pcp) e gera um pacote de patches Windows Installer (pacote. msp). Chamar [Msimsp.exe](msimsp-exe.md) é o método recomendado para usar [Patchwiz.dll](patchwiz-dll.md). A função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) está disponível na versão 4,0 do Patchwiz.dll e estende a funcionalidade da função UiCreatePatchPackage.

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
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

Local para arquivos temporários. Esse parâmetro pode ser **nulo** ou uma cadeia de caracteres vazia, mas não pode ser omitido. O local padrão é% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

Se **for true**, remova a pasta temporária e todo o seu conteúdo, se presente. Se **false** e a pasta estiver presente, a função falhará.

</dd> </dl>

## <a name="return-values"></a>Valores de retorno

Consulte a tabela em [valores de retorno para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Comentários

para obter um exemplo de como criar um arquivo. pcp e usar o UiCreatePatchPackage para gerar um pacote de patches Windows Installer, consulte a seção [um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md).

A criação de um patch requer uma imagem de instalação descompactada, como uma imagem administrativa ou uma imagem de instalação descompactada de um CD-ROM. UiCreatePatchPackage não gera patches binários para arquivos em gabinetes.

 

 



