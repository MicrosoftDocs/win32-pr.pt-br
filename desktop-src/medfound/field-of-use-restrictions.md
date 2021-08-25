---
description: Campo de restrições de uso
ms.assetid: 36f28e4c-2baf-4618-9935-5d4615f6bc77
title: Campo de restrições de uso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccfb5b7c0923bdea117371a3b6af2669bf903fb3af996f754be43d5665c1ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942658"
---
# <a name="field-of-use-restrictions"></a>Campo de restrições de uso

> [!Note]  
> este tópico aplica-se ao Windows 7 ou posterior.

 

Uma restrição *de campo de uso* é um provisionamento que limita como uma licença para uma tecnologia específica pode ser usada.

Media Foundation fornece um mecanismo para impor restrições de campo de uso em transformações de Media Foundation (MFTs), especialmente em codecs. Esse mecanismo exige que o MFT bloqueie seu próprio uso por aplicativos até que o aplicativo tenha executado um handshake com o MFT. Media Foundation não define o handshake — normalmente, ele envolveria algum tipo de troca de criptografia.

### <a name="registration-and-enumeration"></a>Registro e enumeração

Se uma MFT tiver restrições de campo de uso, defina o sinalizador **\_ FIELDOFUSE do \_ sinalizador \_ de enumeração de MFT** ao registrar o MFT. Esse sinalizador se aplica às seguintes APIs de registro de MFT:

-   [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
-   [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)
-   [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)
-   [**IMFLocalMFTRegistration::RegisterMFTs**](/windows/desktop/api/mfidl/nf-mfidl-imflocalmftregistration-registermfts)

Por padrão, o MFTs registrado com esse sinalizador é excluído dos resultados da enumeração. Para enumerar MFTs com restrições de campo de uso, chame [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) e especifique o **sinalizador \_ \_ \_ FIELDOFUSE do sinalizador de enumeração de MFT** no parâmetro *flags* . O diagrama a seguir ilustra esse processo.

![diagrama mostrando MFT e um aplicativo enviando dados para o registro](images/mft-fou01.gif)

A função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) sempre exclui qualquer MFTs que tenha restrições de campo de uso.

### <a name="unlocking-the-mft"></a>Desbloqueando o MFT

Para usar uma MFT com restrições de campo de uso, execute as seguintes etapas:

1.  O aplicativo implementa a interface [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) .
2.  O método [**IMFFieldOfUseMFTUnlock:: Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) usa um ponteiro para a interface **IUnknown** do MFT.
3.  No método [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) , o aplicativo executa o handshake necessário, usando qualquer mecanismo definido pela MFT. Esta etapa não é definida pela API Media Foundation.
4.  Se o método [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) for executado com sucesso, o MFT se desbloqueará.

O aplicativo especifica o ponteiro [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) definindo o atributo [de \_ \_ \_ atributo de desbloqueio de MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) . Há várias maneiras diferentes de definir esse atributo, dependendo de como seu aplicativo cria o decodificador ou o pipeline de codificação:



| API                   | Como desbloquear o campo de uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Leitor de origem         | Se seu aplicativo usar o [leitor de origem](source-reader.md) para decodificar um arquivo de mídia, defina o atributo [ \_ \_ \_ atributo de desbloqueio de MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) nos parâmetros de configuração. Consulte [atributos do leitor de origem](source-reader-attributes.md).                                                                                                                                                                                                                                                                         |
| Gravador do coletor           | Se seu aplicativo usar o gravador de coletor para codificar um arquivo de mídia, defina o atributo [ \_ \_ \_ atributo de desbloqueio de MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) nos parâmetros de configuração. Consulte [atributos do gravador do coletor](sink-writer-attributes.md).                                                                                                                                                                                                                                                                                                    |
| Transcodificação rápida        | Se seu aplicativo usar o recurso de transcodificação rápida para criar uma topologia de codificação, defina o [ \_ \_ \_ atributo de desbloqueio de MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) ao chamar [**IMFTranscodeProfile:: setcontainerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Para obter mais informações sobre o recurso de transcodificação rápida, consulte [API de transcodificação](transcode-api.md).                                                                                                                                                                      |
| Topologia              | Se você criar uma topologia diretamente, defina o [ \_ atributo FIELDOFUSE \_ de \_ desbloqueio de MFT](mft-fieldofuse-unlock-attribute.md) como um atributo na topologia. Consulte [atributos de topologia](topology-attributes.md).                                                                                                                                                                                                                                                                                                                                                  |
| Objeto de ativação de MFT | Se seu aplicativo enumerar diretamente os decodificadores ou codificadores que ele usará, defina o [ \_ atributo FIELDOFUSE de \_ desbloqueio \_ de MFT](mft-fieldofuse-unlock-attribute.md) nos ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) . <br/> Defina o atributo antes de chamar [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para criar o MFT. O objeto de ativação chama [**IMFFieldOfUseMFTUnlock:: Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) quando cria o MFT.<br/> |



 

O diagrama a seguir mostra a relação entre os objetos de ativação de MFT e a interface [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) .

![diagrama mostrando um aplicativo, um objeto de ativação e uma MFT com setas para um objeto fou, que tem uma seta de volta para o MFT](images/mft-fou02.gif)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




