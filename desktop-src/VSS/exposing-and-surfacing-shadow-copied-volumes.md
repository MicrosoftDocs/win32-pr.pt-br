---
description: Além de serem acessados por meio da interface IVssBackupComponents por meio do objeto de dispositivo da sua cópia, um solicitante pode disponibilizar uma cópia de sombra para outros processos como um dispositivo somente leitura montado.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Expondo e Identificandondo volumes copiados de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781486"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a>Expondo e Identificandondo volumes copiados de sombra

Além de serem acessados por meio da interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) por meio do [*objeto de dispositivo*](vssgloss-d.md)da sua cópia, um solicitante pode disponibilizar uma cópia de sombra para outros processos como um dispositivo somente leitura montado.

Esse processo é conhecido como [*expor uma cópia de sombra*](vssgloss-e.md)e é executado usando o método [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) .

Uma cópia de sombra pode ser exposta como um volume local, atribuída uma letra de unidade ou associada a uma pasta montada — ou como um compartilhamento de arquivos.

Para ilustrar, considere uma cópia de sombra feita de um volume no sistema exposedSys montada em F: \\ on cuja raiz são os diretórios dirOne e dirTwo e o arquivo FileOne.

## <a name="exposing-a-shadow-copy-locally"></a>Expondo uma cópia de sombra localmente

Quando montado como um volume local, a raiz da cópia de sombra fica sempre visível no ponto de montagem (letra da unidade ou pasta montada) e todos os arquivos copiados por sombra são visíveis.

Se a cópia de sombra tiver sido exposta localmente por meio da pasta montada C: \\ ShadowOfF, você encontrará todos os arquivos presentes no disco montado em F: \\ no momento da cópia de sombra disponível em C: \\ ShadowOfF. Examinar C: \\ ShadowOfF revelaria dois diretórios, dirOne e dirTwo, e um arquivo, fileone, em C: \\ ShadowOfF.

Uma chamada para expor localmente a cópia de sombra pode ser:

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

Se a cópia de sombra tiver sido exposta com êxito localmente, *wszExposed* deverá conter a cadeia de caracteres larga "C: \\ ShadowOfF".

A cópia de sombra pode ser desexposta posteriormente chamando [**IVssBackupComponentsEx2:: UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).

Somente as cópias de sombra persistentes, ou seja, cópias de sombra criadas com a \_ reversão do VSS CTX \_ nas \_ Rollback ou a \_ reversão do aplicativo CTX do VSS \_ \_ , podem ser expostas localmente.

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a>Expondo uma cópia de sombra como um compartilhamento remoto

Como alternativa, você pode optar por fazer a cópia de sombra do disco montado em F: \\ disponível como um compartilhamento de arquivos remoto e expor apenas os dados em dirTwo como o compartilhamento de arquivos dirTwoOfF.

Nesse caso, os sistemas podiam acessar a cópia de sombra dos arquivos em F: \\ dirTwo mapeando \\ \\ exposedSys \\ dirTwoOfF como uma unidade de rede.

Uma chamada para implementar a exposição remota da cópia de sombra como um compartilhamento pode ser a seguinte:

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

Se a cópia de sombra tiver sido exposta com êxito remotamente, *wszExposed* deverá conter a cadeia de caracteres largo "dirTwoOfF".

Qualquer sistema que atualmente mapeie o compartilhamento de rede do dirTwoOfF poderia se desconectar dele, assim como ele pode se desconectar de qualquer compartilhamento comum.

## <a name="surfacing-a-shadow-copy"></a>Identificando uma cópia de sombra

Uma [*cópia de sombra na superfície*](vssgloss-s.md) é aquela em que a cópia de sombra é conhecida por um namespace do Gerenciador de montagem do sistema.

Isso significa que você pode localizar essas cópias de sombra assim como você localizaria qualquer outro volume disponível, mas ainda não montado, usando **FindFirstVolume** e **FindNextVolume**, por exemplo.

Claramente, as cópias de sombra expostas também são cópias de sombra em superfície. No entanto, o inverso não é necessariamente verdadeiro.

Se uma cópia de sombra exposta localmente foi desmontada ou um sistema optou por desconectar uma cópia de sombra exposta remotamente, essa cópia de sombra não seria mais exposta. No entanto, desde que a cópia de sombra persista, os volumes seriam exibidos. Isso significa que eles podem ser montados como qualquer outro volume somente leitura.

 

 



