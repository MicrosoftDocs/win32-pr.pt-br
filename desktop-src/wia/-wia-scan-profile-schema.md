---
description: O esquema do perfil de verificação define um formato XML que pode ser usado para armazenar as propriedades de itens de aquisição de imagem do Windows (WIA), como scanners e câmeras.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Esquema do perfil de verificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c52e933e1e6b771c477bdc8a38f1c5f749448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759851"
---
# <a name="scan-profile-schema"></a><span data-ttu-id="7f9e9-103">Esquema do perfil de verificação</span><span class="sxs-lookup"><span data-stu-id="7f9e9-103">Scan Profile Schema</span></span>

<span data-ttu-id="7f9e9-104">O esquema do perfil de verificação define um formato XML que pode ser usado para armazenar as propriedades de itens de aquisição de imagem do Windows (WIA), como scanners e câmeras.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-104">The Scan Profile Schema defines an XML format that can be used to store the properties of Windows Image Acquisition (WIA) items, such as scanners and cameras.</span></span> <span data-ttu-id="7f9e9-105">Esses arquivos persistentes permitem que os aplicativos forneçam verificação automática sem exigir que os usuários se lembrem das configurações de propriedade dos itens.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-105">These persistent files enable applications to provide automatic scanning without requiring users to remember the property settings of the items.</span></span>

<span data-ttu-id="7f9e9-106">Qualquer dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) pode ter um perfil de verificação.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-106">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="7f9e9-107">No entanto, **IWiaItem2** itens dos \_ tipos \_ grupo WIA concluído \_ arquivo e \_ raiz da categoria WIA \_ não podem ter perfis.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-107">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="7f9e9-108">Os perfis de verificação são criados e gerenciados por meio das interfaces [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md)e [**IScanProfileUI**](-wia-iscanprofileui.md) .</span><span class="sxs-lookup"><span data-stu-id="7f9e9-108">Scan profiles are created and managed through the [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md), and [**IScanProfileUI**](-wia-iscanprofileui.md) interfaces.</span></span> <span data-ttu-id="7f9e9-109">Os usuários do seu aplicativo podem modificar perfis de maneiras limitadas usando o método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="7f9e9-109">Users of your application can modify profiles in limited ways using the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="7f9e9-110">Todos os perfis de verificação têm os seguintes elementos: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` e `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="7f9e9-110">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="7f9e9-111">O perfil padrão de um dispositivo também tem um `<Default>` elemento.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-111">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="7f9e9-112">O `<ProfileGUID>` elemento e o `<DeviceID>` elemento não podem ser alterados depois que o perfil de verificação é criado.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-112">The `<ProfileGUID>` element and the `<DeviceID>` element cannot be changed after the scan profile is created.</span></span> <span data-ttu-id="7f9e9-113">Os valores do `<ProfileName>` elemento e do `<WiaItem>` elemento podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-113">The values of the `<ProfileName>` element and the `<WiaItem>` element can be modified.</span></span> <span data-ttu-id="7f9e9-114">O `<Default>` elemento pode ser adicionado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-114">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="7f9e9-115">Isso pode ser feito de forma programática usando os métodos [**IScanProfile:: SetName**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) .</span><span class="sxs-lookup"><span data-stu-id="7f9e9-115">This can be done programatically using the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="7f9e9-116">Essas propriedades também podem ser alteradas pelos usuários por meio do método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="7f9e9-116">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="7f9e9-117">O `<Properties>` elemento contém `<Property>` filhos.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-117">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="7f9e9-118">Use-os para adicionar qualquer item WIA ou propriedade de dispositivo ao perfil.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-118">Use these to add any WIA item or device property to the profile.</span></span> <span data-ttu-id="7f9e9-119">Você também pode desenvolver sua própria imagem aquisição `<Property>` filhos.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-119">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="7f9e9-120">Isso torna o esquema do perfil de verificação extensível.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-120">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="7f9e9-121">(Para obter mais informações sobre como estender o esquema, consulte [definindo propriedades personalizadas](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).)</span><span class="sxs-lookup"><span data-stu-id="7f9e9-121">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

<span data-ttu-id="7f9e9-122">Aqui está o esquema completo do perfil de verificação.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-122">Here is the complete Scan Profile Schema.</span></span> <span data-ttu-id="7f9e9-123">Segue um exemplo de perfil.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-123">A sample profile follows.</span></span>


```
<?xml version="1.0"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema"
            targetNamespace="https://www.microsoft.com"
            xmlns="https://www.microsoft.com"
            elementFormDefault="qualified">

<xs:element name="ScanProfile">
            <xs:complexType>
            <xs:sequence>
                        <xs:element name="ProfileGUID" type="xs:string"/>
                        <xs:element name="DeviceID" type="xs:string"/>
<xs:element name="ProfileName" type="xs:string"/>
                        <xs:element name="Default" minOccurs="0">
                                    <xs:complexType>
                                    </xs:complexType>
                        </xs:element>
                        <xs:element name="WiaItem" type="xs:string"/>
                        <xs:element name="Properties" type="Properties"/>
            </xs:sequence>
            </xs:complexType>
</xs:element>
 
<xs:complexType name="Properties">
<xs:sequence>
            <xs:element name="Property" maxOccurs="unbounded" minOccurs="0">
            <xs:complexType>
            <xs:simpleContent>
                        <xs:extension base="xs:string">
                                    <xs:attribute name="id" type="xs:integer" use="required"/>
                                    <xs:attribute name="type" type="xs:integer" use="required"/>
                        </xs:extension>
            </xs:simpleContent>
            </xs:complexType>
            </xs:element>
</xs:sequence>
</xs:complexType>
 
</xs:schema>
```



<span data-ttu-id="7f9e9-124">Clique em **Mostrar exemplo** para ver um perfil de exemplo.</span><span class="sxs-lookup"><span data-stu-id="7f9e9-124">Click **Show Example** to see a sample profile.</span></span>


```
<ScanProfile>
    <ProfileGUID>
        {F862E217-32B0-4396-987A-2191224925CD}
    </ProfileGUID>
    <DeviceID>
        {6BDD1FC6-810F-11D0-BEC7-08002BE2092F}\0001
    </DeviceID>
    <ProfileName>
        Last used settings
    </ProfileName>
    <WiaItem>
        {FB607B1F-43F3-488B-855B-FB703EC342A6}
    </WiaItem>
    <Properties>
        <Property id="4103" type="3">
            3
        </Property>
        <Property id="4106" type="72">
            {B96B3CAB-0728-11D3-9D7B-0000F81EF32E}
        </Property>
        <Property id="6147" type="3">
            300
        </Property>
        <Property id="6154" type="3">
            0
        </Property>
        <Property id="6155" type="3">
            0
        </Property>
    </Properties>
</ScanProfile>
```



## <a name="related-topics"></a><span data-ttu-id="7f9e9-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f9e9-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7f9e9-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7f9e9-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7f9e9-127">**IScanProfile:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="7f9e9-127">**IScanProfile::GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[<span data-ttu-id="7f9e9-128">**IScanProfile:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="7f9e9-128">**IScanProfile::SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)
</dt> <dt>

<span data-ttu-id="7f9e9-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="7f9e9-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7f9e9-130">Constantes da propriedade WIA</span><span class="sxs-lookup"><span data-stu-id="7f9e9-130">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="7f9e9-131">Definindo propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="7f9e9-131">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



