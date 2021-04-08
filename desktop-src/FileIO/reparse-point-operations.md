---
description: Descreve as operações de ponto de nova análise que você pode executar usando DeviceIoControl.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Operações de ponto de nova análise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011530"
---
# <a name="reparse-point-operations"></a>Operações de ponto de nova análise

Para determinar se um sistema de arquivos dá suporte a pontos de nova análise, chame a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examine se o **arquivo dá suporte ao sinalizador de bit de \_ \_ \_ pontos de nova análise** .

A função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) permite que você defina, modifique, obtenha e remova pontos de nova análise. A tabela a seguir descreve as operações de ponto de nova análise que você pode executar usando **DeviceIoControl**.



| Operação                                                           | Descrição                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**FSCTL \_ definir \_ ponto de nova análise \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | Permite que o programa de chamada defina um novo ponto de nova análise ou modifique um existente.<br/> |
| [**FSCTL \_ obter \_ ponto de nova análise \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | Obtém as informações armazenadas em um ponto de nova análise existente.<br/>                         |
| [**FSCTL \_ excluir \_ ponto de nova análise \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | Remove um ponto de nova análise existente.<br/>                                                   |



 

Se você estiver modificando, obtendo ou excluindo um ponto de nova análise, deverá especificar a mesma marca de nova análise na operação contida no arquivo. Caso contrário, a operação falhará com a **\_ \_ \_ incompatibilidade de erros de reanálise de erro** de erro. Se você estiver modificando ou excluindo um ponto de nova análise, também deverá especificar o **GUID** de nova análise na operação contida no arquivo. Caso contrário, a operação falhará com o **erro de erro ao \_ reanalisar o \_ \_ conflito de atributo**.

Para determinar se um arquivo ou diretório contém um ponto de nova análise, use a função [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) . Se o arquivo ou diretório tiver um ponto de nova análise associado, o atributo de **\_ \_ \_ ponto de nova análise de atributo de arquivo** será definido.

Para substituir um ponto de nova análise existente sem que já tenha um identificador para o arquivo ou diretório, chame [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o **sinalizador de arquivo \_ \_ abrir \_ \_ ponto de nova análise**. Esse sinalizador permite que você abra o arquivo se o filtro do sistema de arquivos correspondente está ou não instalado e funcionando corretamente.

 

