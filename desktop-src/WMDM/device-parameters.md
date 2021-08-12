---
title: Parâmetros do dispositivo
description: Parâmetros do dispositivo
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows Gerenciador de Dispositivos de mídia, parâmetros de dispositivo
- Gerenciador de Dispositivos, parâmetros do dispositivo
- Guia de programação, parâmetros do dispositivo
- provedores de serviço, parâmetros do dispositivo
- criando provedores de serviços, parâmetros de dispositivo
- parâmetros do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef097940670148551042c22fd8efc6aa51c641960bf0f821361aaf3c29c731d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585345"
---
# <a name="device-parameters"></a>Parâmetros do dispositivo

Windows A mídia Gerenciador de Dispositivos usa parâmetros de dispositivo para controlar o comportamento de um dispositivo. Esses parâmetros são adicionados ao registro conforme especificado no arquivo de instalação do dispositivo (arquivo INF). a tabela a seguir lista os parâmetros de dispositivo que Windows mídia Gerenciador de Dispositivos consultas.



| Nome do parâmetro do dispositivo | Tipo de dados do registro | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *WMDMSPCLSID*         | **REG \_ sz**        | Valor que especifica o CLSID do provedor de serviços que controla este dispositivo. Esse parâmetro é obrigatório para suporte a PnP.<br/> O valor do parâmetro deve ser o CLSID, não o ProgID do provedor de serviços. esse parâmetro é obrigatório para dar suporte a Plug and Play (PnP) em Windows Gerenciador de Dispositivos de mídia. Para obter mais informações, consulte [habilitando PNP para dispositivos](enabling-pnp-for-devices.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *OptimalTransferSize* | **REG \_ DWORD**     | valor opcional que especifica o tamanho de transferência preferencial que Windows mídia Gerenciador de Dispositivos usa durante as operações de leitura e gravação. Se não for fornecido, será usado um tamanho de transferência padrão.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *UseMetadataViews*    | **REG \_ DWORD**     | parâmetro opcional que especifica se Windows mídia Gerenciador de Dispositivos organiza o conteúdo pelos metadados enquanto apresenta o conteúdo do dispositivo aos aplicativos. Se não for especificado, o valor padrão será 0.<br/> quando os aplicativos enumeram o conteúdo nos armazenamentos de um player de áudio portátil, Windows mídia Gerenciador de Dispositivos pode apresentar o conteúdo organizado por metadados. Isso é especialmente útil para dispositivos com grande capacidade de armazenamento.<br/> Aplicativos e dispositivos têm a capacidade de controlar esse comportamento. Os dispositivos indicam sua preferência por meio do parâmetro de dispositivo *UseMetadataViews*.<br/> Há suporte para os dois valores inteiros a seguir:<br/> Solicita que o conteúdo seja apresentado aos aplicativos exatamente como organizado no sistema de arquivos do dispositivo.<br/> Solicita que o conteúdo seja apresentado aos aplicativos organizados por metadados.<br/> |
| *ShowInShell*         | **REG \_ DWORD**     | parâmetro opcional que especifica se o dispositivo deve aparecer no Windows Explorer. o valor 1 indica que o dispositivo deve aparecer no Windows Explorer. para obter mais informações, consulte [requisitos para players de áudio portáteis a serem exibidos no Windows Explorer](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *UseExtendedWmdm*     | **REG \_ DWORD**     | parâmetro opcional que alerta Windows mídia Gerenciador de Dispositivos que o provedor de serviços dá suporte a **IMDSPDevice3**, **IMDSPObject2** e **IMDSPStorage4**. sem esse sinalizador, Windows mídia Gerenciador de Dispositivos nunca chamará essas interfaces. O valor 1 indica que há suporte para essas interfaces.<br/> Esse sinalizador é necessário para provedores de serviço que sincronizam com Windows Media Player. (Consulte [habilitando a sincronização com o Windows Media Player](enabling-synchronization-with-windows-media-player.md)).<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

**Codificando o arquivo INF**

O código de exemplo a seguir do arquivo INF de um dispositivo demonstra a definição de alguns parâmetros de dispositivo durante a instalação do dispositivo.


```C++
; Set parameters on Windows 95 and Windows 98 operating systems.
[DriverInstall.hw]
AddReg=DriverHwPropReg

; Set parameters on Windows NT-based operating systems.
[DriverInstall.NT.hw]
AddReg=DriverHwPropReg

; Related section that specifies the device parameters.
[DriverHwPropReg]
; Add your own CLSID here.
HKR,,WMDMSPCLSID,,"{00000000-0000-0000-0000-000000000000}"
HKR,,OptimalTransferSize,0x10001,0x10000
HKR,,UseMetadataViews,0x10001,0x1
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> <dt>

[**Interface IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)
</dt> <dt>

[**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[**Interface IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





