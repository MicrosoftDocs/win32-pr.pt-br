---
description: A criação de uma pasta montada é um processo de duas etapas.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Criando pastas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3067af38a893085adcc407263711c80a64c3eea1e535f6814db2cd2742f899
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650226"
---
# <a name="creating-mounted-folders"></a>Criando pastas montadas

A criação de uma pasta montada é um processo de duas etapas. Primeiro, chame [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) com o ponto de montagem (letra da unidade, caminho do GUID do volume ou pasta montada) do volume a ser atribuído à pasta montada. Em seguida, use a função [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para associar o caminho do GUID do volume retornado ao diretório desejado em outro volume. Para obter um exemplo de código, consulte [criando uma pasta montada](mounting-a-volume-at-a-mount-point.md).

Seu aplicativo pode designar qualquer diretório vazio em um volume diferente da raiz como uma pasta montada. Quando você chama a função [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , esse diretório se torna a pasta montada. Você pode atribuir o mesmo volume a várias pastas montadas.

Depois que a pasta montada tiver sido estabelecida, ela será mantida por meio da reinicialização do computador automaticamente.

Se um volume falhar, todos os volumes que foram atribuídos a pastas montadas nesse volume não poderão mais ser acessados por meio dessas pastas montadas. Por exemplo, suponha que você tenha dois volumes, C: e D:, e que D: esteja associado à pasta montada C: montado \\ \\ . Se o volume C: falhar, o volume D: não poderá mais ser acessado por meio do caminho C: \\ montado \\ .

Somente volumes do sistema de arquivos NTFS podem ter pastas montadas, mas os volumes de destino para as pastas montadas podem ser volumes não NTFS.

As pastas montadas são implementadas usando pontos de nova análise e estão sujeitas às suas restrições. Para obter mais informações, consulte [pontos de nova análise](reparse-points.md). Não é necessário manipular pontos de nova análise para usar pastas montadas; funções como [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) lidam com todos os detalhes do ponto de nova análise para você.

Como as pastas montadas são diretórios, você pode renomear, remover, mover e, de outra forma, manipulá-los, como faria com outros diretórios.

(Observação: a documentação do TechNet usa o termo *unidades montadas* para se referir a *pastas montadas*.)

 

 



