---
description: A propriedade FASTOEM foi projetada para permitir que os OEMs reduzam o tempo necessário para instalar Windows Installer aplicativos para um cenário específico.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: Propriedade FASTOEM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754359"
---
# <a name="fastoem-property"></a>Propriedade FASTOEM

A propriedade **FASTOEM** foi projetada para permitir que os OEMs reduzam o tempo necessário para instalar Windows Installer aplicativos para um cenário específico. Não crie a propriedade **FASTOEM** na tabela de [Propriedades](property-table.md).

A propriedade **FASTOEM** só será aplicável se todas essas condições forem verdadeiras:

-   O aplicativo está sendo instalado no mesmo volume que a pasta que contém os arquivos de origem.
-   Os arquivos de origem são excluídos após a instalação.
-   Nenhuma interface do usuário é exibida durante a instalação. O [nível da interface do usuário](user-interface-levels.md) é nenhum.
-   A instalação é executada no [contexto de instalação](installation-context.md)por máquina.
-   Há espaço suficiente no computador para uma instalação bem-sucedida.
-   Essa é a primeira vez que a instalação. A instalação não está anunciando, reinstalando, removendo ou fazendo uma instalação administrativa.
-   Nenhum recurso está instalado para ser executado da origem.
-   O pacote de instalação não contém [componentes isolados](isolated-components.md). Como os componentes isolados exigem que os arquivos de origem permaneçam localizados na origem, a propriedade **FASTOEM** não pode ser usada atualmente com componentes isolados.

Se todas as condições anteriores forem verdadeiras, a configuração da propriedade **FASTOEM** permitirá que Windows Installer melhore o desempenho fazendo o seguinte:

-   Mover em vez de copiar arquivos no mesmo volume. Isso não garante que todos os arquivos sejam movidos em vez de copiados. Observe que, se o computador tiver vários discos rígidos, você deverá inicializar a propriedade [**ROOTDRIVE**](rootdrive.md) na linha de comando para a mesma unidade que contém a origem da instalação.
-   Omita essa fonte da lista de origem do aplicativo para que as instalações de reinstalação ou manutenção subsequentes sejam padronizadas para as fontes de CD-ROM especificadas na [tabela de mídia](media-table.md).
-   Simplifique o [custo do arquivo](file-costing.md).
-   Suprimir mensagens de progresso enviadas do Windows Installer ao cliente.

## <a name="remarks"></a>Comentários

Como nenhuma mensagem de progresso é enviada quando **FASTOEM** é definido, é recomendável que os autores gravem manualmente um valor de 1800 para tempo limite na chave

**HKLM** \\ **Software** \\ **Políticas** \\ do **Microsoft** \\ **Windows** \\ **Instalador** \\ do **Tempo limite**

Timeout é um tipo **reg \_ DWORD** .

Para exibir o tamanho do aplicativo em Adicionar ou remover programas no painel de controle do Windows 2000, você deve gravar manualmente o valor de EstimatedSize na chave

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ o **<  Código > do produto**

Esse é um tipo **reg \_ DWORD** e é igual ao tamanho do aplicativo em Kbytes. O instalador não grava esse valor automaticamente.

Use a seguinte linha de comando de exemplo se o CD-ROM enviado para os usuários finais armazenar o pacote de instalação do aplicativo na raiz do CD-ROM. Observe que o rótulo de volume na [tabela de mídia](media-table.md) do arquivo. msi deve corresponder ao rótulo de volume do CD-ROM.

**Msiexec/I C: \\ TempImage \\package.msi/qn/Le logfile.txt AllUsers = 1 FASTOEM = 1 DISABLEROLLBACK = 1 ROOTDRIVE = C:\\**

Use a seguinte linha de comando de exemplo se o pacote de instalação não estiver localizado na raiz do CD-ROM enviado aos usuários finais. Você deve definir a propriedade [**MEDIAPACKAGEPATH**](mediapackagepath.md) nesse caso como o caminho para o pacote de instalação. O rótulo de volume na [tabela de mídia](media-table.md) do arquivo. msi deve corresponder ao rótulo de volume do CD-ROM. Nesse caso, siga este exemplo.

**Msiexec/I C: \\ TempImage \\package.msi/qn/Le logfile.txt AllUsers = 1 FASTOEM = 1 DISABLEROLLBACK = 1 MEDIAPACKAGEPATH = c: \\ TempImage \\package.msi ROOTDRIVE = c:\\**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




