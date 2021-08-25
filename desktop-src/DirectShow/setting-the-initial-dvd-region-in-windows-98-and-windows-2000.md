---
description: Configurando a região do DVD inicial
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Configurando a região do DVD inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bf019c7d5ddae8efb257435e1b23037575a37f809ef012190b49c619cc3211
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102316"
---
# <a name="setting-the-initial-dvd-region"></a>Configurando a região do DVD inicial

É responsabilidade do fabricante do sistema selecionar uma região de DVD inicial para a unidade de DVD em seus PCs.

> [!Note]  
> Somente discos criptografados podem ser usados para definir a região.

 

### <a name="windows-2000-and-later"></a>Windows 2000 e posterior

a partir do Windows 2000, a região de DVD padrão é selecionada com base na localidade para a qual o computador está configurado. Windows 2000 sempre definirá a região inicial para uma unidade de DVD usando essa região padrão, bem como a região do disco, se houver um disco na unidade. o fabricante do sistema não precisa fazer nada para definir a região inicial para as unidades de DVD Windows 2000 ou posteriores.

Para unidades RPC1, se não houver nenhum disco na unidade durante a inicialização, a região padrão será definida com base apenas na localidade da máquina. Se houver um disco de DVD na unidade durante a inicialização, a região padrão será selecionada para ser a região da unidade, desde que ela corresponda a uma região do disco; caso contrário, a região mais baixa no disco será escolhida como a região inicial da unidade. O usuário (ou fabricante do sistema) tem uma alteração restante permitida, caso o padrão não esteja correto.

para unidades RPC2, se durante o processo de instalação Windows 2000 descobre que a unidade não tem nenhuma região definida, ele tentará escolher uma região como acima, mas somente se houver um disco na unidade. (As unidades RPC1 escolherão a região sem nenhum disco na unidade). Depois que uma região é definida para unidades RPC2, ela não é alterada automaticamente por uma reinstalação ou por uma instalação limpa do sistema operacional.

O OEM pode definir uma chave do registro que contém a região do DVD padrão para o sistema. Na primeira inicialização, a região da unidade será definida com esse valor. a chave do registro no Windows 2000 e posterior é HKLM \\ System \\ CurrentControlSet \\ Control \\ classe \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion (binary).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte à alteração da região do DVD no Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



