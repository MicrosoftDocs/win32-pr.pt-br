---
description: usando a exclusão mútua para o ASF Fluxos
ms.assetid: fdd31eac-1dd6-45f0-90fb-d5a74c85db2e
title: usando a exclusão mútua para o ASF Fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c7fd104659064952803c16f572ee1e55dee0508144474e89ee7c0f362315c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034555"
---
# <a name="using-mutual-exclusion-for-asf-streams"></a>usando a exclusão mútua para o ASF Fluxos

O conteúdo do ASF pode conter vários fluxos mutuamente exclusivos. Esses fluxos não podem ser lidos simultaneamente, mas apenas um deles é lido por vez. Por exemplo, o arquivo pode conter um conjunto de fluxos que inclui o mesmo conteúdo codificado em uma taxa de bits diferente. O fluxo usado é determinado pela largura de banda disponível para o aplicativo que transmite o conteúdo. O objeto de exclusão mútua do ASF, que faz parte do objeto de cabeçalho, armazena informações sobre o grupo de fluxos mutuamente exclusivos.

No Media Foundation, o objeto de *exclusão mútua* que expõe a interface [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) existe para cada objeto de exclusão mútua de ASF. O objeto de perfil contém referência a todos os objetos de exclusão mútua.

O objeto de exclusão mútua armazena informações sobre o grupo de fluxos mutuamente exclusivos como registros. Um objeto de exclusão mútua pode ter vários registros que podem ser usados para criar cenários complexos. Cada registro contém um ou mais fluxos que não podem coexistir com fluxos em outro registro, mantidos pelo objeto de exclusão mútua, dependendo do tipo de exclusão mútua, como taxa de bits.

Um exemplo comum de exclusão mútua complexa é um arquivo que contém três fluxos de áudio do mesmo conteúdo em várias taxas de bits em cada uma das três linguagens. Apenas um dos nove fluxos deve ser reproduzido por vez, mas há dois tipos pelos quais eles são mutuamente exclusivos: a taxa de idioma e de bits.

Para este exemplo, os nove fluxos recebem os seguintes números de fluxo:

<dl> 1-idioma 1, taxa de bits 1  
2-idioma 1, taxa de bits 2  
3-idiomas 1, taxa de bits 3  
4-idiomas 2, taxa de bits 1  
5-idioma 2, taxa de bits 2  
6-idiomas 2, taxa de bits 3  
7-Idioma 3, taxa de bits 1  
8-idiomas 3, taxa de bits 2  
9-idioma 3, taxa de bits 3  
</dl>

Esse cenário pode ser implementado usando os quatro objetos de exclusão mútua a seguir:

-   O primeiro objeto de exclusão mútua inclui os fluxos 1, 2 e 3, mutuamente exclusivos por taxa de bits. Cada fluxo tem seu próprio registro.
-   O segundo objeto de exclusão mútua inclui fluxos de 4, 5 e 6, mutuamente exclusivos por taxa de bits. Cada fluxo tem seu próprio registro.
-   O terceiro objeto de exclusão mútua inclui 7, 8 e 9, mutuamente exclusivo por taxa de bits. Cada fluxo tem seu próprio registro.
-   O quarto objeto de exclusão mútua contém três registros, o primeiro, incluindo os fluxos 1, 2 e 3; o segundo inclui fluxos 4, 5 e 6; e o terceiro, incluindo o streams 7, 8 e 9. Esses registros são mutuamente exclusivos por idioma.

Ao reproduzir um arquivo criado dessa forma, o aplicativo de streaming seleciona o idioma primeiro, pois é menos provável que seja alterado no meio da apresentação e, em seguida, seleciona uma taxa de bits.

## <a name="mutual-exclusion-object-creation-and-configuration"></a>Criação e configuração de objeto de exclusão mútua

A lista a seguir resume o processo de configuração de um objeto de exclusão mútua:

1.  Crie um objeto de exclusão mútua.
2.  Defina o tipo de exclusão mútua.
3.  Configure o objeto de exclusão mútua adicionando registros e os fluxos associados.
4.  Adicione o objeto de exclusão mútua ao perfil.

Para criar e configurar um objeto de exclusão mútua

1.  Chame [**IMFASFProfile:: CreateMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion) para criar um objeto de exclusão mútua vazio.
2.  Chame [**IMFASFMutualExclusion:: SetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype) para definir o critério do fluxo mutuamente exclusivo.

    Os fluxos podem ser mutuamente exclusivos por idioma, taxa de bits, apresentação e critérios personalizados. O tipo é representado como um GUID. Para obter uma lista dessas constantes, consulte [GUIDs do tipo de exclusão mútua do ASF](asf-mutual-exclusion-type-guids.md).

3.  Chame [**IMFASFMutualExclusion:: AddRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord) para adicionar um registro ao objeto de exclusão mútua.

    Esse método adiciona um registro vazio e atribui a ele um índice de registro que começa com zero.

4.  Chame [**IMFASFMutualExclusion:: AddStreamForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addstreamforrecord) para adicionar o número de fluxo ao registro especificado pelo índice de registro.

    Cada registro inclui um ou mais fluxos. Cada fluxo em um registro é mutuamente exclusivo de todos os fluxos em todos os outros registros. Para obter o número de fluxos em um registro, chame [**IMFASFMutualExclusion:: GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord) especificando o índice de registro.

    Para remover um fluxo do registro, chame [**IMFASFMutualExclusion:: RemoveStreamFromRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removestreamfromrecord) e especifique o índice do registro e o número do fluxo.

5.  Chame [**IMFASFProfile:: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) para adicionar o objeto de exclusão mútua configurado ao perfil.

## <a name="enumerating-mutual-exclusion-objects-in-a-profile"></a>Enumerando objetos de exclusão mútua em um perfil

Se [**IMFASFProfile:: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) tiver sucesso, ele atribuirá um índice ao objeto especificado, começando em zero.

Para enumerar os objetos de exclusão mútua associados a um perfil, chame [**IMFASFProfile:: GetMutualExclusionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount) e execute o loop pela lista chamando [**IMFASFProfile:: GetMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion). Os índices de exclusão mútua são sequenciais e variam entre 0 e um menor que o número de fluxos recuperados por **GetMutualExclusionCount**.

Um objeto de exclusão mútua é removido do perfil chamando [**IMFASFProfile:: RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion). O perfil reatribui os índices de exclusão mútua para que eles sejam sequenciais a partir de zero. Isso substitui os índices armazenados anteriormente, que não são mais válidos depois de chamar esse método. Isso libera os registros de fluxo de exclusão mútua associados.

## <a name="removing-records-in-a-mutual-exclusion-object"></a>Removendo registros em um objeto de exclusão mútua

Para remover um registro de um objeto de exclusão mútua, chame [**IMFASFMutualExclusion:: RemoveRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord). Se esse método for bem sucedido, o objeto de exclusão mútua indexa os registros restantes para que eles sejam sequenciais a partir de zero. O aplicativo deve enumerar os registros para garantir o índice correto para cada registro. Para fazer isso, chame [**IMFASFMutualExclusion:: GetRecordCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getrecordcount) e execute o loop pelos registros chamando [**IMFASFMutualExclusion:: GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord).

A remoção do registro com o índice mais alto não tem nenhum efeito sobre os outros índices.

## <a name="modifying-a-mutual-exclusion-object"></a>Modificando um objeto de exclusão mútua

Para alterar a configuração do objeto de exclusão mútua no perfil, o aplicativo deve substituir o objeto de exclusão mútua existente por outro objeto que contém as novas configurações.

Para alterar a configuração do objeto de exclusão mútua no perfil

1.  Enumere os objetos de exclusão mútua no perfil para obter o objeto que precisa ser alterado.
2.  Chame [**IMFASFMutualExclusion:: clone**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-clone) para clonar o objeto de exclusão mútua.

3.  Configure o objeto clonado conforme necessário.
4.  Chame [**IMFASFProfile:: RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion) para remover o antigo objeto de exclusão mútua do perfil.

5.  Chame [**IMFASFProfile:: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) para adicionar o objeto de exclusão mútua atualizado ao perfil.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perfil ASF](asf-profile.md)
</dt> </dl>

 

 



