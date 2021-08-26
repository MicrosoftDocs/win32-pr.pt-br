---
description: O formato de disco rígido virtual (VHD) é uma especificação de formato de imagem disponível publicamente que permite o encapsulamento do disco rígido em um arquivo individual para uso pelo sistema operacional como um disco virtual de todas as mesmas maneiras que discos rígidos físicos são usados.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Sobre o VHD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a79bd7695144811a1ec98f79e736760bbaddc8ef4b7460e55c5a66353a0b2ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865947"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span id="vhd.about_vhd"></span>Sobre o VHD

O formato de disco rígido virtual (VHD) é uma [especificação](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) de formato de imagem disponível publicamente que permite o encapsulamento do disco rígido em um arquivo individual para uso pelo sistema operacional como um *disco virtual* de todas as mesmas maneiras que discos rígidos físicos são usados. Esses discos virtuais são capazes de hospedar sistemas de arquivos nativos (NTFS, FAT, exFAT e UDFS) enquanto dão suporte a operações de arquivo e disco padrão. O suporte à API do VHD permite o gerenciamento dos discos virtuais. Os discos virtuais criados com a API VHD podem funcionar como discos de inicialização.

um exemplo de como os arquivos VHD são usados é o recurso do [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) no Windows 7, Windows server 2008, servidor virtual e Windows virtual PC. esses produtos usam a API do VHD para conter o Windows imagem do sistema operacional utilizada por uma máquina virtual como seu disco de inicialização do sistema.

o SDK (Software Development Kit) do Microsoft Windows integra o suporte nativo do VHD para trabalhar com discos virtuais, facilitando para os desenvolvedores e administradores criar, gerenciar e implantar imagens Windows em arquivos VHD usando o suporte à API de plataforma ou ferramentas de gerenciamento. Não é necessário instalar aplicativos separados ou implementar um analisador de formato VHD para habilitar essas operações. Essas APIs permitem o uso genérico de discos virtuais independentemente de outras tecnologias de virtualização.

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminologia

O termo *repositório de backup* é usado para fazer referência ao arquivo físico que existe no disco rígido real. O repositório de backup é representado por um *arquivo de imagem VHD*.

Os termos *dinâmicos*, *expansíveis* e *esparsos* costumam ser usados de maneira intercambiável ao se referir a discos virtuais expansíveis dinamicamente. Para a tecnologia VHD, esses termos são idênticos.

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Visão geral dos recursos do sistema VHD

O diagrama a seguir apresenta uma visão geral dos recursos do VHD e suas relações.

![diagrama de bloco VHD](images/vhd.png)

Veja a seguir uma explicação resumida dos recursos descritos anteriormente.

APIs de Windows nativas de modo de usuário:

-   VirtDisk.dll-biblioteca comum para APIs de gerenciamento de VHD.

Wrappers de gerenciamento específicos de domínio do modo de usuário:

-   [apis VHD do vds](/windows/desktop/VDS/about-vds) – wrappers do modelo de objeto vds para as apis de Windows do VHD.

Drivers de modo kernel:

-   Enumerador de unidade virtual de VDrvRoot.sys raiz.
-   Gerenciamento de dependência de volume aninhado por FsDepends.sys.
-   Vhdmp.sys-analisador de VHD e provedor de propriedade de dependência.

a documentação do SDK nesta seção aborda as APIs do VHD Windows do modo de usuário nativo.

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Tipos de disco virtual

Há considerações para usar discos virtuais e quais tipos de discos virtuais estão disponíveis:

-   **Corrigido**– o arquivo de imagem VHD é previamente alocado no repositório de backup para o tamanho máximo solicitado.
-   **Expansível**– também conhecido como "dinâmico", "expansível dinamicamente" e "esparso", o arquivo de imagem VHD usa apenas o espaço no armazenamento de backup, conforme necessário, para armazenar os dados reais que o disco virtual contém atualmente. Ao criar esse tipo de disco virtual, a API VHD não testa o espaço livre no disco físico com base no tamanho máximo solicitado, portanto, é possível criar com êxito um disco virtual dinâmico com um tamanho máximo maior do que o espaço livre disponível no disco físico. Para obter mais informações, consulte [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).
    **Observação**  O tamanho máximo de um disco virtual dinâmico é de 2.040 GB.

     

-   **Diferenciação**— um disco virtual pai é usado como base desse tipo, com quaisquer gravações subsequentes gravadas no disco virtual como diferenças no novo arquivo de imagem VHD diferencial e o arquivo de imagem VHD pai não é modificado. Por exemplo, se você tiver um disco virtual do sistema operacional de inicialização do sistema de instalação limpa como pai e designar o disco virtual diferencial como o disco virtual atual para o sistema usar, o sistema operacional no disco virtual pai permanecerá em seu estado original para recuperação rápida ou para criar rapidamente mais imagens de inicialização com base em discos virtuais diferenciais adicionais. Para obter mais informações, consulte [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).
    **Observação**  O tamanho máximo de um disco virtual diferencial é de 2.040 GB.

     

Todos os tipos de disco virtual têm um tamanho mínimo de 3 MB.

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Tópicos relacionados

[Sobre o VDS](/windows/desktop/VDS/about-vds)

[Referência do VHD](vhd-reference.md)

[Especificação de formato de imagem de disco rígido virtual](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
