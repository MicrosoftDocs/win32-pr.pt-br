---
description: Adicionando uma letra de unidade a um LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Adicionando uma letra de unidade a um LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 388c59a2e1b719e792855460f45fa0c04add7502f8e06aba56f0416a212a9aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755495"
---
# <a name="adding-a-drive-letter-to-a-lun"></a>Adicionando uma letra de unidade a um LUN

\[a partir do Windows 8 e Windows Server 2012, a interface COM do [serviço de disco Virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de Armazenamento Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Você pode atribuir letras de unidade a objetos de volume diretamente; no entanto, se o disco for um objeto de LUN, você terá algumas etapas adicionais.

**Para atribuir uma letra da unidade a um objeto LUN**

1.  Se necessário, desmascarar o LUN para o host local.
    > [!Note]  
    > Você não pode executar operações administrativas de software em um objeto de LUN que não é mascarado para outro computador na sessão VDS atual.

     

2.  Invoque o método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) no computador que está executando o provedor de hardware.
3.  Inicialize o LUN como um disco básico da seguinte maneira:
    1.  Invoque o método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto LUN para consultar a interface [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) .
    2.  Invoque o método [**IVdsSwProvider:: createpack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para criar um pacote básico.
    3.  Invoque o método [**IVdsPack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para adicionar o disco ao novo pacote.
4.  Crie uma partição no disco e obtenha o objeto de volume da seguinte maneira:
    1.  Invoque o método [**IVdsCreatePartitionEx:: CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) para criar uma partição.
    2.  Invoque o método [**IVdsAsync:: Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) no objeto Async que é retornado por [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) para obter o identificador de volume da estrutura [**de \_ \_ saída do VDS Async**](/windows/desktop/api/Vds/ns-vds-vds_async_output) .
    3.  Passe o identificador de volume como um parâmetro para o método [**IVdsService:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) para obter um ponteiro de objeto de volume.
5.  Invoque o método [**IVdsVolumeMF:: AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) para atribuir a letra da unidade.

> [!Note]  
> O método [**IVdsAdvancedDisk:: AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) atribui letras de unidade a partições sem volumes associados, como partições OEM ou ESP. Você não pode usá-lo para atribuir uma letra de unidade a um objeto LUN.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando VDS](using-vds.md)
</dt> <dt>

[**IVdsService:: reenumerar**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[**IVdsSwProvider:: createpack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[**IVdsAsync:: aguardar**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**saída do VDS \_ assíncrono \_**](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
